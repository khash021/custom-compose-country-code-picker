[![](https://jitpack.io/v/khash021/custom-compose-country-code-picker.svg)](https://jitpack.io/#khash021/custom-compose-country-code-picker)


# Custom Compose Country Code Picker

Custom Compose Country Code Picker (built based off of [joelkanyi's Kompose Country Code Picker](https://github.com/joelkanyi/kompose-country-code-picker)) is a  Material 3 (M3) Jetpack Compose library that provides a
country code picker for Android apps.

This provides more UI customization with the ability to modify all text styles, paddings, icons and much more. Refer to the main function's (`CustomComposeCountryCodePicker`) docs for detailed explanation of all parameters

See the [project's website](https://joelkanyi.github.io/kompose-country-code-picker/) for
documentation.

#### Add the dependency to your dependencies block in your app's build.gradle file:
```kotlin
dependencies {
    implementation("com.github.khash021:custom-compose-country-code-picker:<latest-version>")
}
```

#### Usage Example
```kotlin
var phoneNumber by rememberSaveable { mutableStateOf("") }
val state = rememberKomposeCountryCodePickerState(
    // limitedCountries = listOf("KE", "UG", "TZ", "RW", "SS"),
    showCountryCode = true,
    showCountryFlag = true,
    defaultCountryCode = "US",
)

CustomComposeCountryCodePicker(
    modifier = Modifier.fillMaxWidth(),
    state = state,
    text = phoneNumber,
    onValueChange = {
        phoneNumber = it
    },
)
```

## Preview

 Picker                                          | Dialog                                          | Picker Only                                          
-------------------------------------------------|-------------------------------------------------|------------------------------------------------------
 <img src="docs/assets/picker.png" width="250"/> | <img src="docs/assets/dialog.png" width="250"/> | <img src="docs/assets/picker-only.png" width="250"/> 

### Translations
This project includes translations for the following languages:

- **Arabic (ar)**:
- **German (de)**:
- **Spanish (es)**:
- **French (fr)**:
- **Hindi (hi)**:
- **Italian (it-IT)**:
- **Dutch (nl)**:
- **Russian (ru-RU)**:
- **Swahili (sw)**:
- **Turkish (tr-TR)**:
- **Indonesia (in-rID)**:

If your language is not included in the translations, or if you notice any errors in the current translations, please [open an issue](https://github.com/joelkanyi/kompose-country-code-picker/issues) on GitHub. Your contribution will be highly appreciated!


## License

```
Copyright 2023 Joel Kanyi

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

 http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
