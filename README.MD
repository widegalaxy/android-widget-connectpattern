# ConnectPatternView

A widget that can be used to confirm the user's action, unlocking the screen etc. by providing the desired pattern with specified configuration.
Widget can be animated in and out.

![Nine connectors](http://i.giphy.com/qw030BgWy58I.gif) ![Five connectors](http://i.giphy.com/awDeJACJcZTCU.gif) <br/> ![Three connectors](http://i.giphy.com/J5B3NZzyNU3zG.gif) ![Two connectors](http://i.giphy.com/CQND8zKV33Vpm.gif)

## Features

- Widget can contain different number of connectors: 2, 3, 5 or 9.
- Size and color of the connector (circle by default) can be specified in the xml.
- Width and color of the connecting lines can be specified in the xml.
- Connector can be defined as a drawable so any image or icon can be specified in the xml.


## Adding it to your project

    compile 'com.bcgdv.asia.lib:connectpattern:0.1'
    
## Usage

### The connect pattern needs to be configured in the XML.

```xml
<com.bcgdv.asia.lib.connectpattern.ConnectPatternView
    android:id="@+id/connect"
    android:padding="32dp"
    android:layout_width="350dp"
    android:layout_height="350dp"
    android:layout_centerVertical="true"
    android:layout_centerHorizontal="true"
    app:connectPatternNumber="nine"
    app:connectPatternCircleColor="@color/colorPrimary"
    app:connectPatternLineColor="@color/colorAccent"
    app:connectPatternCircleRadius="14dp"
    app:connectPatternLineWidth="7dp"
    app:connectPatternDrawable="@mipmap/ic_star"/>
```

- `app:connectPatternNumber` (Optional) - determines how many connectors will be used
- `app:connectPatternCircleColor` (Optional) - color of the circle
- `app:connectPatternCircleRadius` (Optional) - radius of the circle
- `app:connectPatternLineColor` (Optional) - color of the connecting lines
- `app:connectPatternLineWidth` (Optional) - width of the connecting lines
- `app:connectPatternDrawable` (Optional) - custom icon / image / drawable to use instead of circle


## Callbacks

```java
view.setOnConnectPatternListener(new ConnectPatternView.OnConnectPatternListener() {
        @Override
        public void onPatternEntered(ArrayList<Integer> result) {
        }

        @Override
        public void onPatternAbandoned() {
        }

        @Override
        public void animateInStart() {
        }

        @Override
        public void animateInEnd() {
        }

        @Override
        public void animateOutStart() {
        }

        @Override
        public void animateOutEnd() {
        }
    });
```