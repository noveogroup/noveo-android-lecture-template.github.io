## Animate View State Changes


    <selector xmlns:android="http://schemas.android.com/apk/res/android">
        <item android:state_pressed="true">
            <set>
              <objectAnimator android:propertyName="translationZ"
                android:duration="@android:integer/config_shortAnimTime"
                android:valueTo="2dp"
                android:valueType="floatType"/>
        </set>
        </item>
            <item android:state_enabled="true"
              android:state_pressed="false"
              android:state_focused="true">
                <set>
                  <objectAnimator android:propertyName="translationZ"
                    android:duration="100"
                    android:valueTo="0"
                    android:valueType="floatType"/>
                </set>
        </item>
    </selector>