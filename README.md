# Android-TicketView

An Android Library used to implement TicketView based on [vipulasri/TicketView Library](https://github.com/vipulasri/TicketView) in android with normal, rounded and scallop corners + some extra exciting features.

### Specs
[![API](https://img.shields.io/badge/API-19%2B-brightgreen.svg?style=flat)](https://android-arsenal.com/api?level=19)
[![MethodsCount](https://img.shields.io/badge/Methods%20and%20size-125%20|%2012KB-e91e63.svg)](http://www.methodscount.com/?lib=com.vipulasri%3Aticketview%3A1.0.2)
[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](https://github.com/vipulasri/Timeline-View/blob/master/LICENSE)

### Badges/Featured In
[![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-Ticket%20View-brightgreen.svg?style=flat)](https://android-arsenal.com/details/1/6521)
[![AndroidDev Digest](https://img.shields.io/badge/AndroidDev%20Digest-%23171-blue.svg)](https://www.androiddevdigest.com/digest-171/)

![showcase](https://github.com/passid-services/Android-TicketView/blob/master/art/Screenshot_1.png | width=100)
![showcase](https://github.com/passid-services/Android-TicketView/blob/master/art/Screenshot_2.png | width=100)
![showcase](https://github.com/passid-services/Android-TicketView/blob/master/art/Screenshot_3.png | width=100)
![showcase](https://github.com/passid-services/Android-TicketView/blob/master/art/Screenshot_4.png | width=100)
![showcase](https://github.com/passid-services/Android-TicketView/blob/master/art/Screenshot_5.png | width=100)

## Sample Project

For information : checkout [Sample App Code](https://github.com/passid-services/Android-TicketView/tree/master/example) in repository.

## Quick Setup

### 1. Include library

**Using Gradle**

``` gradle
dependencies {
    implementation 'com.passid.android:ticketview:1.0.0'
}
```

**Using Maven**

``` maven
<dependency>
    <groupId>com.passid.android</groupId>
    <artifactId>ticketview</artifactId>
    <version>1.0.0</version>
    <type>pom</type>
</dependency>
```

### 2. Usage
 * In XML Layout :

``` java
<com.passid.android.ticketview.TicketView
    android:layout_width="match_parent"
    android:layout_height="160dp"
    android:layout_marginTop="60dp"
    android:layout_marginLeft="20dp"
    android:layout_marginRight="20dp"
    android:id="@+id/ticketView"
    app:ticketBackgroundColor="@color/grey"
    app:ticketCornerRadius="8dp"
    app:ticketCornerType="rounded"
    app:ticketDividerColor="#FFFFFF"
    app:ticketDividerDesign="color"
    app:ticketDividerLocation="left"
    app:ticketDividerPadding="5dp"
    app:ticketDividerType="dash"
    app:ticketDividerWidth="1dp"
    app:ticketElevation="0dp"
    app:ticketOrientation="horizontal"
    app:ticketPunchLocation="left|right"
    app:ticketPunchRadius="12dp"
    app:ticketScallopRadius="0dp"
    app:ticketShowBorder="false"
    app:ticketShowDivider="true"
    app:view="@id/anchoredViewId">

    <androidx.constraintlayout.widget.ConstraintLayout
        android:layout_width="match_parent"
        android:layout_height="64dp"
        android:background="?selectableItemBackground">

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="match_parent"
            android:gravity="center_vertical"
            android:paddingStart="24dp"
            android:text="Group Ticket."
            android:textColor="#fff"
            android:textSize="18sp"
            android:textStyle="bold"
            app:layout_constraintStart_toStartOf="parent" />

        <FrameLayout
            android:id="@+id/anchoredViewId"
            android:layout_width="wrap_content"
            android:layout_height="match_parent"
            android:layout_gravity="end"
            android:paddingStart="22dp"
            android:paddingEnd="22dp"
            app:layout_constraintEnd_toEndOf="parent">

            <TextView
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_gravity="center"
                android:background="#f00"
                android:gravity="center"
                android:paddingStart="10dp"
                android:paddingEnd="10dp"
                android:text="USD $200"
                android:textColor="#000"
                android:textSize="14sp"
                android:textStyle="bold" />

        </FrameLayout>

    </androidx.constraintlayout.widget.ConstraintLayout>

</com.passid.android.ticketview.TicketView>
```

* Configure using xml attributes or setters in code:

    <table>
    <th>Attribute Name</th>
    <th>Default Value</th>
    <th>Description</th>
    <tr>
        <td>app:ticketOrientation="vertical"</td>
        <td>horizontal</td>
        <td>sets orientation of divider and scallop</td>
    </tr>
    <tr>
        <td>app:ticketBackgroundColor="@android:color/black"</td>
        <td>white</td>
        <td>sets background color</td>
    </tr>
    <tr>
        <td>app:ticketScallopRadius="10dp"</td>
        <td>20dp</td>
        <td>sets scallop radius</td>
    </tr>
    <tr>
        <td>app:ticketShowBorder="false"</td>
        <td>false</td>
        <td>shows border if `true`</td>
    </tr>
    <tr>
        <td>app:ticketBorderWidth="4dp"</td>
        <td>2dp</td>
        <td>sets border width</td>
    </tr>
    <tr>
        <td>app:ticketBorderColor="@color/grey"</td>
        <td>black</td>
        <td>sets border color</td>
    </tr>
    <tr>
        <td>app:ticketShowDivider="true"</td>
        <td>false</td>
        <td>shows divider if `true`</td>
    </tr>
    <tr>
        <td>app:ticketDividerType="dash"</td>
        <td>normal</td>
        <td>sets type of divider ie `normal` or `dash`</td>
    </tr>
    <tr>
        <td>app:ticketDividerDesign="punch"</td>
        <td>0dp</td>
        <td>sets the design of the designer either `color` or `punch` (punch will show as cut through displaying the background behind the ticketView.</td>
    </tr>
    <tr>
        <td>app:ticketDividerColor="@color/colorAccent"</td>
        <td>dark gray</td>
        <td>sets divider color</td>
    </tr>
    <tr>
        <td>app:ticketDividerWidth="2dp"</td>
        <td>2dp</td>
        <td>sets divider width</td>
    </tr>
    <tr>
        <td>app:ticketDividerPadding="0dp"</td>
        <td>10dp</td>
        <td>sets divider padding</td>
    </tr>
    <tr>
        <td>app:ticketDividerDashGap="4dp"</td>
        <td>4dp</td>
        <td>sets divider dash gap</td>
    </tr>
    <tr>
        <td>app:ticketDividerDashLength="8dp"</td>
        <td>8dp</td>
        <td>sets divider dash length</td>
    </tr>
    <tr>
        <td>app:ticketCornerType="rounded"</td>
        <td>normal</td>
        <td>sets type of corner ie `normal` or `rounded` or `scallop`</td>
    </tr>
    <tr>
        <td>app:ticketCornerRadius="15dp"</td>
        <td>4dp</td>
        <td>sets corner radius if corner rounder or scallop</td>
    </tr>
    <tr>
        <td>app:ticketElevation="14dp"</td>
        <td>0dp</td>
        <td>sets elevation to ticket view on android jellybean and above</td>
    </tr>
    <tr>
        <td>app:ticketDividerLocation="none|left|right|top|bottom"</td>
        <td>none</td>
        <td>sets the location of the divider and scallops with regards to the anchored view app:view</td>
    </tr>
    <tr>
        <td>app:view="@id/anchoredViewId"</td>
        <td>@null</td>
        <td>sets the view id in which the divider will be anchored to based on flags of app:ticketDividerLocation and ticketOrientation</td>
    </tr>
    <tr>
        <td>app:ticketPunchLocation="none|left|right|top|bottom"</td>
        <td>none</td>
        <td>Set the location where a punch through holes will be drawn on the sides of the ticket</td>
    </tr>
    <tr>
        <td>app:ticketPunchRadius="12dp"</td>
        <td>0dp</td>
        <td>sets the radius of the punch through holes.</td>
    </tr>
    </table>


## License


    Copyright 2017 Vipul Asri

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
