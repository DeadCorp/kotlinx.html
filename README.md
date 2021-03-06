[![Official JetBrains Project](http://jb.gg/badges/official.svg)](https://confluence.jetbrains.com/display/ALL/JetBrains+on+GitHub)
[![Download](https://api.bintray.com/packages/kotlin/kotlinx.html/kotlinx.html/images/download.svg)](https://bintray.com/kotlin/kotlinx.html/kotlinx.html/_latestVersion)  [![npm](https://img.shields.io/npm/v/kotlinx-html.svg)](https://www.npmjs.com/package/kotlinx-html) [![TeamCity (simple build status)](https://img.shields.io/teamcity/http/teamcity.jetbrains.com/s/KotlinTools_KotlinxHtml_Build.svg)](https://teamcity.jetbrains.com/viewType.html?buildTypeId=KotlinTools_KotlinxHtml_Build&branch_Kotlin_KotlinX=%3Cdefault%3E&tab=buildTypeStatusDiv&guest=1) [ ![Kotlin](https://img.shields.io/badge/Kotlin-1.2.71-orange.svg) ](https://kotlinlang.org/) [![GitHub license](https://img.shields.io/badge/license-Apache%20License%202.0-green.svg?style=flat)](http://www.apache.org/licenses/LICENSE-2.0)

# kotlinx.html

A kotlinx.html library provides DSL to build HTML to [Writer](http://docs.oracle.com/javase/8/docs/api/java/io/Writer.html)/[Appendable](http://docs.oracle.com/javase/8/docs/api/java/lang/Appendable.html) or DOM at JVM and browser (or other JavaScript engine) for 
better [Kotlin programming](http://kotlinlang.org) for Web. 

# Get started

See [Getting started](https://github.com/kotlin/kotlinx.html/wiki/Getting-started) page for details how to include the library

# DOM
You can build DOM tree with JVM and JS naturally

See example for JavaScript-targeted Kotlin

```kotlin
window.setInterval({
    val myDiv = document.create.div("panel") {
        p { 
            +"Here is "
            a("http://kotlinlang.org") { +"official Kotlin site" } 
        }
    }

    document.getElementById("container")!!.appendChild(myDiv)

    document.getElementById("container")!!.append {
        div {
            +"added it"
        }
    }
}, 1000L)
```

# Stream
You can build HTML directly to Writer (JVM only) or Appendable (both JVM and JS)

```kotlin
System.out.appendHTML().html {
    body {
        div {
            a("http://kotlinlang.org") {
                target = ATarget.blank
                +"Main site"
            }
        }
    }
}
```

# Documentation

See [wiki](https://github.com/kotlin/kotlinx.html/wiki) pages

# Building 
See [development](https://github.com/kotlin/kotlinx.html/wiki/Development) page for details
