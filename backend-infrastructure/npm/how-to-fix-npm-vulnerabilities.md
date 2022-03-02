# how to fix npm vulnerabilities

#### Vulnerabilities

You can get a report of all vulnerabilities using `npm audit`. In that report for each vulnerability you will also see a way to fix it. When you use `npm audit fix` you are telling npm to execute those fixes. Npm however will not automatically install fixes that might break your project, such as major versions changes. You'll have to manually execute the `npm install` commands for those if you decide the vulnerability is more important than having to deal with the possible breaking change.

_Note:_ Since writing, `npm audit fix --force` was introduced which will even execute patches that might introduce breaking changes. Use at your own risk, I've used it and it ended badly, very badly.



reference: [https://stackoverflow.com/questions/59922953/fix-vulnerabilities-in-npm-manually](https://stackoverflow.com/questions/59922953/fix-vulnerabilities-in-npm-manually)
