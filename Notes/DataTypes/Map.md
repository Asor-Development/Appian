# Maps
-  an ad-hoc data structure created inline in an expression using the `a!map()` function
- **single map:** a!map(name: "Shannon", favColor: "Purple")
- **array of maps:** {a!map(name: "Shannon", favColor: "Purple"), a!map(name: "Keya", favColor: "Blue")}
- helps avoids conversions/casting
- fields within a map that contain data queries may be evaluated in parallel to reduce the overall evaluation time