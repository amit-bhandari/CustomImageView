# CustomImageView
Custom Image View with capability of setting image url from xml

Simple Image View class extended from Image View to support data binding in Android.

You can set url of this image view directly from xml. Will be useful if you are using data binding for binding url variable directly to imageview. No more findViewById in your code.

Dependecy -> [Glide](https://github.com/bumptech/glide) 
You can use any library you want for that matter, just make changes at couple locations in MyImageView.kt

#### How to use this Image View?

Copy MyImageView.kt in your code

Create attr.xml in res/values if does not exists already

Enter attribute as following in attr.xml

```xml
    <declare-styleable name="MyImageView">
        <attr name="url" format="string" />
    </declare-styleable>
```

And you are good to go to use it as your image view in xml.

```xml
        <package.path.MyImageView
             android:id="@+id/image_company_logo"
             android:scaleType="fitCenter"
             android:layout_width="match_parent"
             android:layout_height="80dp"
             android:contentDescription="logo"
             app:url="@{invoice.invoiceLogoLink}"/>  //for data binding purpose
```

# Cheers
