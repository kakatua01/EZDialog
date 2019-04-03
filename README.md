# EZDialog
[![](https://jitpack.io/v/Binary-Finery/EZDialog.svg)](https://jitpack.io/#Binary-Finery/EZDialog)

- min SDK 17
- written in Java

Extremely simple to use and highly customisable alert dialog library

To see this library in action, you can download the demo app from Google Playstore by clicking [here](https://play.google.com/store/apps/details?id=com.spencerstudios.ezdialogdemoapp) 

## Installation

Add this into your root build.gradle file:

```java
allprojects {
	repositories {
		...
		maven { url 'https://jitpack.io' }
	}
}
```

Add the dependency to your module build.gradle:

```java
dependencies {
	implementation 'com.github.Binary-Finery:EZDialog:1.0.4'
}
```

## Example Usage

```java

//build a simple dialog...

new EZDialog.Builder(this)
	.setTitle("EXDialog")
	.setMessage("EZDialog example")
	.setPositiveBtnText("okay")
	.setNegativeBtnText("close")
	.setCancelableOnTouchOutside(false)
	.OnPositiveClicked(new EZDialogListener() {
		@Override
		public void OnClick() {
			//todo
                 }
	})
	.OnNegativeClicked(new EZDialogListener() {
		@Override
                 public void OnClick() {
                 	//todo
                    }
                })
	.build();
	
//all available methods

.setTitle(String);
.setMessage(String);
.setPositiveBtnText(String);
.setNegativeBtnText(String) ;
.setNeutralBtnText(String);
.showTitleDivider(boolean);
.setTitleDividerLineColor(int);
.setTitleTextColor(int);
.setMessageTextColor(int);
.setBackgroundColor(int);
.setHeaderColor(int);
.setButtonTextColor(int);
.OnPositiveClicked(EZDialogListener);
.OnNegativeClicked(EZDialogListener);
.OnNeutralClicked(EZDialogListener);
.setAnimation(Animation);
.setCancelableOnTouchOutside(boolean);
.setFont(Font);
.setCustomFont(int);
.build();
```
