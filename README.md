# Activity

## In-line preferences:
   CheckBoxPreference

    <PreferenceCategory
        android:title="In-line preferences"
        android:key="pref_key_storage_settings">
        <CheckBoxPreference
            android:key="pref_key_auto_delete"
            android:summary="This is a checkbox"
            android:title="CheckBoxPreference"
            android:defaultValue="false"/>
    </PreferenceCategory>
    
  ![Image text](https://github.com/chenzifeng123/image/blob/master/4_001.PNG)
    
## Dialog-based preferences:
  EditTextPreference;
  ListPreference
  
    <PreferenceCategory
        android:title="Dialog-based preferences"
        android:key="pref_key_storage_settings2">
        <EditTextPreference
            android:dialogTitle="Enter your favorite animal"
            android:key="editTitlePreference"
            android:summary="An example that uses an edit txt dialog"
            android:title="Edit text preference"
            />
        <ListPreference
            android:defaultValue="001"
            android:dialogTitle="Choose one"
            android:entries="@array/listChange"
            android:entryValues="@array/listChange_value"
            android:key="List_change_Preference"
            android:summary="An example that uses an edit list dialog"
            android:title="List preference"
            />
    </PreferenceCategory>
    
    
  ![Image text](https://github.com/chenzifeng123/image/blob/master/4_002.PNG)
  ![Image text](https://github.com/chenzifeng123/image/blob/master/4_003.PNG)
    
## Launch preferences:
   PreferenceScreen: 跳转到另一个PreferenceScreen;
   PreferenceScreen: 启动一个网页 
   
    <PreferenceCategory
        android:title="Launch preferences"
        android:key="pref_key_storage_settings3">
        <PreferenceScreen
            android:key="button_voicemail_category_key1"
            android:title="Screen preference"
            android:summary="Shows another screen of preferences"
            android:persistent="false">
            <CheckBoxPreference
                android:key="PreferenceScreen_checkbox"
                android:summary="Preference that is on the next screen but same hierarchy"
                android:title="Toggle preference"
                android:defaultValue="false" />
        </PreferenceScreen>
        <PreferenceScreen
            android:key="button_voicemail_category_key2"
            android:title="Intent preference"
            android:summary="Launches an Activity from an Intent"
            android:persistent="false">
            <intent android:action="android.intent.action.VIEW"
                android:data="http://www.example.com" />
        </PreferenceScreen>
    </PreferenceCategory>
    
![Image text](https://github.com/chenzifeng123/image/blob/master/4_004.PNG)
![Image text](https://github.com/chenzifeng123/image/blob/master/4_005.PNG)
    
## Preference attributes 
   CheckBox: 父选项;
   CheckBox: 子选项，当父选项勾选时呈现
   
     <PreferenceCategory
        android:title="Preference attributes "
        android:key="pref_key_storage_settings4">
        <CheckBoxPreference
            android:key="parent_checkbox"
            android:summary="This is visually a parent"
            android:title="Parent checkbox preference"
            android:defaultValue="false" />
        <CheckBoxPreference
            android:key="child_checkbox"
            android:dependency="parent_checkbox"
            android:summary="This is visually a child"
            android:title="Child checkbox preference"
            android:defaultValue="false" />
     </PreferenceCategory>
     
![Image text](https://github.com/chenzifeng123/image/blob/master/4_001.PNG)
![Image text](https://github.com/chenzifeng123/image/blob/master/4_006.PNG)
