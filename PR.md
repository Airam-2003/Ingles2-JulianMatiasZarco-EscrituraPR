## Purpose
This PR aims to correct several issues in the WeatherApp project that affected both user experience and system reliability. 

The primary goal is to ensure the application displays accurate weather data, handles API errors gracefully, and provides a consistent and accessible interface for users.


## Context
Previously, the WeatherApp displayed temperature values in Kelvin, which was confusing for most users accustomed to the Celsius scale. 

Other main problems included:
- Lack of proper error handling in the fetchWeatherData() function, which caused the app to crash when the API request failed.
- Unclosed HTML tags in the WeatherCard component, leading to misaligned elements.
- Inconsistent use of CSS units (px and rem), affecting the app’s responsiveness on different devices.
- Missing localization support, with all error messages hard-coded in English.


## Highlighting changes and impact

To address these issues, the following modifications were implemented:

- Added temperature conversion from Kelvin to Celsius in WeatherDisplay.js, ensuring data matches users’ expectations.
- Added robust error handling in fetchWeatherData() to prevent crashes during network or API failures.
- Fixed unclosed tags in WeatherCard.jsx, improving layout stability and visual consistency.
- Standardized all CSS units to rem for better responsiveness across various screen sizes.
- Added Spanish translations for error messages using a simple localization module to enhance accessibility.

These changes aim to improve the usability, stability, and inclusivity of the app. Users now receive clear, localized feedback and can rely on accurate weather information even under poor network conditions.



## Feedback

Please review the updated WeatherDisplay.js and fetchWeatherData() implementations carefully.

Also, LMK if there are any problems with the new error-handling logic or if additional test cases are needed for the localization feature.

## Final comments

TL;DR: The PR aimed to fix incorrect temperature units, improves error handling, repairs layout bugs, and adds localization.

Moving forward, we should consider adding automated tests for translation consistency, allowing userd to change the temperature display from Celsius to Kelvin, and possibly extend support for more languages beyond English and Spanish.

TSYM for taking the time to review this PR and for your continued collaboration on improving WeatherApp. Your feedback is always appreciated!
