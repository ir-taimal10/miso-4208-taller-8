En este punto debido a que no fé facil hacer funcionar stryker con las instrucciones del tutorial quizá por las versiones de la librería.

seguí un tutorial similar: https://github.com/stryker-mutator/robobar-example

La configuración es diferente:
```javascript
module.exports = function(config) {
    config.set({
        mutate: ["src/**/*.js"],
        mutator: "javascript",
        transpilers: [],
        reporters: ["html", "clear-text", "progress"],
        testRunner: "karma",
        testFramework: "jasmine",
        coverageAnalysis: "perTest",
        maxConcurrentTestRunners: 4,
        karma: {
            configFile: "test/config/karma.conf.js",
            config: {
                browsers: ["ChromeHeadless"]
            }
        }
    });
};
```