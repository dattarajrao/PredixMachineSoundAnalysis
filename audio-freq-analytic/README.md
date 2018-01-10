#audio-freq-analysis

A python-based sample analytic for Predix Analytics.

## Analytic template
This analytic takes in an audio file as binary input

## Input format
The expected JSON input data format is as follows:
`{"audio_str": audio_file_string}`

## Output format
The JSON output format from the analytic is as follows:
`{"result":frequency_rpm_array}`

## Developing a Python-based analytic
1. Implement the analytic (and test functions) according to your development guidelines.
2. Create an entry method in your analytic class. The entry method signature must be in one of the following two formats:
 * For analytics that do not use trained models, use the following signature for your entry method:
  `def entry_method(self, inputJson):`
 * For analytics that use trained models, use the following signature for your entry method:
  `def entry_method(self, inputJson, inputModels):`
 * In either case, the `entry_method` can be any method name. `inputJson` is the JSON string input that will be passed to the analytic. The output of this method must also be a JSON string.
 * `inputModels` contains a dict() of trained models as defined in the port-to-field map. The entry method should properly handle the case of an empty dict.
3. Create a config.json file in the top level of the project directory. Specify the entry method in the format of `<subdirectory>.<className>.<methodName>`, conda-libs, and non-conda-libs.
4. Package all the analytic files and the config.json file into a ZIP file.

For more information, see [Python Analytic Development](https://docs.predix.io/en-US/content/service/analytics_services/analytics_framework/analytic-development#concept_9cbf93d9-d4f2-4b42-8695-4c3195f04a79) in the Predix Analytics Services documentation on Predix IO.
