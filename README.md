

/ModLoader/app/src/main/res/layout/plugin_permissions_layout.xml

<?xml version="1.0" encoding="utf-8"?>
<ScrollView xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#F5F5F5">

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical"
        android:padding="16dp">

        <!-- Header -->
        <TextView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="🔐 Plugin Permissions Manager"
            android:textSize="24sp"
            android:textStyle="bold"
            android:textColor="#D32F2F"
            android:gravity="center"
            android:layout_marginBottom="16dp" />

        <!-- Permission Overview Card -->
        <androidx.cardview.widget.CardView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginBottom="16dp"
            app:cardCornerRadius="8dp"
            app:cardElevation="4dp"
            app:cardBackgroundColor="#FFEBEE">

            <LinearLayout
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:orientation="vertical"
                android:padding="16dp">

                <TextView
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:text="📊 Permission Overview"
                    android:textSize="18sp"
                    android:textStyle="bold"
                    android:textColor="#D32F2F"
                    android:layout_marginBottom="8dp" />

                <TextView
                    android:id="@+id/permissionOverviewText"
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:text="🔒 5 plugins with restricted permissions\n🔓 3 plugins with full access\n⚠️ 2 plugins require review"
                    android:textSize="14sp"
                    android:textColor="#C62828"
                    android:lineSpacingExtra="4dp" />

                <Button
                    android:id="@+id/refreshOverviewButton"
                    android:layout_width="wrap_content"
                    android:layout_height="32dp"
                    android:text="🔄 Refresh"
                    android:textSize="12sp"
                    android:background="#D32F2F"
                    android:textColor="#FFFFFF"
                    android:layout_marginTop="8dp"
                    android:minWidth="80dp" />
            </LinearLayout>
        </androidx.cardview.widget.CardView>

        <!-- System-Wide Permission Settings -->
        <androidx.cardview.widget.CardView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginBottom="16dp"
            app:cardCornerRadius="8dp"
            app:cardElevation="4dp"
            app:cardBackgroundColor="#FFFFFF">

            <LinearLayout
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:orientation="vertical"
                android:padding="16dp">

                <TextView
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:text="🛡️ System-Wide Permission Controls"
                    android:textSize="18sp"
                    android:textStyle="bold"
                    android:textColor="#1976D2"
                    android:layout_marginBottom="12dp" />

                <TextView
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:text="Global permission settings that apply to all plugins:"
                    android:textSize="12sp"
                    android:textColor="#666666"
                    android:layout_marginBottom="12dp" />

                <!-- File System Access -->
                <LinearLayout
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:orientation="horizontal"
                    android:gravity="center_vertical"
                    android:padding="8dp"
                    android:background="#F8F9FA"
                    android:layout_marginBottom="8dp">

                    <TextView
                        android:layout_width="0dp"
                        android:layout_weight="1"
                        android:layout_height="wrap_content"
                        android:text="📁 File System Access\nRead/write to app directories"
                        android:textSize="14sp"
                        android:textColor="#333333"
                        android:lineSpacingExtra="2dp" />

                    <Switch
                        android:id="@+id/globalFileSystemPermissionSwitch"
                        android:layout_width="wrap_content"
                        android:layout_height="wrap_content"
                        android:checked="true" />
                </LinearLayout>

                <!-- Network Access -->
                <LinearLayout
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:orientation="horizontal"
                    android:gravity="center_vertical"
                    android:padding="8dp"
                    android:background="#F8F9FA"
                    android:layout_marginBottom="8dp">

                    <TextView
                        android:layout_width="0dp"
                        android:layout_weight="1"
                        android:layout_height="wrap_content"
                        android:text="🌐 Network Access\nInternet connections and downloads"
                        android:textSize="14sp"
                        android:textColor="#333333"
                        android:lineSpacingExtra="2dp" />

                    <Switch
                        android:id="@+id/globalNetworkPermissionSwitch"
                        android:layout_width="wrap_content"
                        android:layout_height="wrap_content"
                        android:checked="false" />
                </LinearLayout>

                <!-- Game Modification -->
                <LinearLayout
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:orientation="horizontal"
                    android:gravity="center_vertical"
                    android:padding="8dp"
                    android:background="#F8F9FA"
                    android:layout_marginBottom="8dp">

                    <TextView
                        android:layout_width="0dp"
                        android:layout_weight="1"
                        android:layout_height="wrap_content"
                        android:text="🎮 Game Modification\nModify game behavior and values"
                        android:textSize="14sp"
                        android:textColor="#333333"
                        android:lineSpacingExtra="2dp" />

                    <Switch
                        android:id="@+id/globalGameModPermissionSwitch"
                        android:layout_width="wrap_content"
                        android:layout_height="wrap_content"
                        android:checked="true" />
                </LinearLayout>

                <!-- Hook Installation -->
                <LinearLayout
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:orientation="horizontal"
                    android:gravity="center_vertical"
                    android:padding="8dp"
                    android:background="#F8F9FA"
                    android:layout_marginBottom="8dp">

                    <TextView
                        android:layout_width="0dp"
                        android:layout_weight="1"
                        android:layout_height="wrap_content"
                        android:text="🔗 Hook Installation\nInstall system and game hooks"
                        android:textSize="14sp"
                        android:textColor="#333333"
                        android:lineSpacingExtra="2dp" />

                    <Switch
                        android:id="@+id/globalHookPermissionSwitch"
                        android:layout_width="wrap_content"
                        android:layout_height="wrap_content"
                        android:checked="true" />
                </LinearLayout>

                <!-- Native Code Execution -->
                <LinearLayout
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:orientation="horizontal"
                    android:gravity="center_vertical"
                    android:padding="8dp"
                    android:background="#FFEBEE"
                    android:layout_marginBottom="8dp">

                    <TextView
                        android:layout_width="0dp"
                        android:layout_weight="1"
                        android:layout_height="wrap_content"
                        android:text="⚡ Native Code Execution\n⚠️ Dangerous: Execute native code"
                        android:textSize="14sp"
                        android:textColor="#D32F2F"
                        android:lineSpacingExtra="2dp" />

                    <Switch
                        android:id="@+id/globalNativeCodePermissionSwitch"
                        android:layout_width="wrap_content"
                        android:layout_height="wrap_content"
                        android:checked="false" />
                </LinearLayout>

                <!-- System Access -->
                <LinearLayout
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:orientation="horizontal"
                    android:gravity="center_vertical"
                    android:padding="8dp"
                    android:background="#FFEBEE">

                    <TextView
                        android:layout_width="0dp"
                        android:layout_weight="1"
                        android:layout_height="wrap_content"
                        android:text="🔧 System Access\n⚠️ Dangerous: Modify system settings"
                        android:textSize="14sp"
                        android:textColor="#D32F2F"
                        android:lineSpacingExtra="2dp" />

                    <Switch
                        android:id="@+id/globalSystemAccessPermissionSwitch"
                        android:layout_width="wrap_content"
                        android:layout_height="wrap_content"
                        android:checked="false" />
                </LinearLayout>
            </LinearLayout>
        </androidx.cardview.widget.CardView>

        <!-- Individual Plugin Permissions -->
        <androidx.cardview.widget.CardView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginBottom="16dp"
            app:cardCornerRadius="8dp"
            app:cardElevation="4dp"
            app:cardBackgroundColor="#FFFFFF">

            <LinearLayout
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:orientation="vertical"
                android:padding="16dp">

                <LinearLayout
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:orientation="horizontal"
                    android:gravity="center_vertical"
                    android:layout_marginBottom="12dp">

                    <TextView
                        android:layout_width="0dp"
                        android:layout_weight="1"
                        android:layout_height="wrap_content"
                        android:text="🔌 Individual Plugin Permissions"
                        android:textSize="18sp"
                        android:textStyle="bold"
                        android:textColor="#7B1FA2" />

                    <Button
                        android:id="@+id/refreshPluginPermissionsButton"
                        android:layout_width="wrap_content"
                        android:layout_height="32dp"
                        android:text="🔄"
                        android:textSize="12sp"
                        android:background="#7B1FA2"
                        android:textColor="#FFFFFF"
                        android:minWidth="48dp" />
                </LinearLayout>

                <TextView
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:text="Configure permissions for each installed plugin:"
                    android:textSize="12sp"
                    android:textColor="#666666"
                    android:layout_marginBottom="8dp" />

                <androidx.recyclerview.widget.RecyclerView
                    android:id="@+id/pluginPermissionsRecyclerView"
                    android:layout_width="match_parent"
                    android:layout_height="300dp"
                    android:background="#FAFAFA"
                    android:padding="8dp" />
            </LinearLayout>
        </androidx.cardview.widget.CardView>

        <!-- Security & Validation Settings -->
        <androidx.cardview.widget.CardView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginBottom="16dp"
            app:cardCornerRadius="8dp"
            app:cardElevation="4dp"
            app:cardBackgroundColor="#E8F5E8">

            <LinearLayout
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:orientation="vertical"
                android:padding="16dp">

                <TextView
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:text="🔒 Security &amp; Validation Settings"
                    android:textSize="18sp"
                    android:textStyle="bold"
                    android:textColor="#2E7D32"
                    android:layout_marginBottom="12dp" />

                <!-- Sandbox Mode -->
                <LinearLayout
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:orientation="horizontal"
                    android:gravity="center_vertical"
                    android:padding="8dp"
                    android:background="#F1F8E9"
                    android:layout_marginBottom="8dp">

                    <TextView
                        android:layout_width="0dp"
                        android:layout_weight="1"
                        android:layout_height="wrap_content"
                        android:text="📦 Enable Sandbox Mode\nIsolate plugin execution"
                        android:textSize="14sp"
                        android:textColor="#2E7D32"
                        android:lineSpacingExtra="2dp" />

                    <Switch
                        android:id="@+id/sandboxModeSwitch"
                        android:layout_width="wrap_content"
                        android:layout_height="wrap_content"
                        android:checked="true" />
                </LinearLayout>

                <!-- Permission Validation -->
                <LinearLayout
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:orientation="horizontal"
                    android:gravity="center_vertical"
                    android:padding="8dp"
                    android:background="#F1F8E9"
                    android:layout_marginBottom="8dp">

                    <TextView
                        android:layout_width="0dp"
                        android:layout_weight="1"
                        android:layout_height="wrap_content"
                        android:text="✅ Strict Permission Validation\nValidate all permission requests"
                        android:textSize="14sp"
                        android:textColor="#2E7D32"
                        android:lineSpacingExtra="2dp" />

                    <Switch
                        android:id="@+id/strictValidationSwitch"
                        android:layout_width="wrap_content"
                        android:layout_height="wrap_content"
                        android:checked="true" />
                </LinearLayout>

                <!-- Auto-deny Dangerous -->
                <LinearLayout
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:orientation="horizontal"
                    android:gravity="center_vertical"
                    android:padding="8dp"
                    android:background="#F1F8E9"
                    android:layout_marginBottom="8dp">

                    <TextView
                        android:layout_width="0dp"
                        android:layout_weight="1"
                        android:layout_height="wrap_content"
                        android:text="🚫 Auto-deny Dangerous Requests\nAutomatically deny risky permissions"
                        android:textSize="14sp"
                        android:textColor="#2E7D32"
                        android:lineSpacingExtra="2dp" />

                    <Switch
                        android:id="@+id/autoDenyDangerousSwitch"
                        android:layout_width="wrap_content"
                        android:layout_height="wrap_content"
                        android:checked="false" />
                </LinearLayout>

                <!-- Require User Confirmation -->
                <LinearLayout
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:orientation="horizontal"
                    android:gravity="center_vertical"
                    android:padding="8dp"
                    android:background="#F1F8E9"
                    android:layout_marginBottom="8dp">

                    <TextView
                        android:layout_width="0dp"
                        android:layout_weight="1"
                        android:layout_height="wrap_content"
                        android:text="👤 Require User Confirmation\nPrompt for sensitive permissions"
                        android:textSize="14sp"
                        android:textColor="#2E7D32"
                        android:lineSpacingExtra="2dp" />

                    <Switch
                        android:id="@+id/requireUserConfirmationSwitch"
                        android:layout_width="wrap_content"
                        android:layout_height="wrap_content"
                        android:checked="true" />
                </LinearLayout>

                <!-- Log Permission Changes -->
                <LinearLayout
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:orientation="horizontal"
                    android:gravity="center_vertical"
                    android:padding="8dp"
                    android:background="#F1F8E9">

                    <TextView
                        android:layout_width="0dp"
                        android:layout_weight="1"
                        android:layout_height="wrap_content"
                        android:text="📝 Log All Permission Changes\nKeep audit trail of changes"
                        android:textSize="14sp"
                        android:textColor="#2E7D32"
                        android:lineSpacingExtra="2dp" />

                    <Switch
                        android:id="@+id/logPermissionChangesSwitch"
                        android:layout_width="wrap_content"
                        android:layout_height="wrap_content"
                        android:checked="true" />
                </LinearLayout>
            </LinearLayout>
        </androidx.cardview.widget.CardView>

        <!-- Permission Actions -->
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="horizontal"
            android:layout_marginBottom="16dp">

            <Button
                android:id="@+id/grantAllSafeButton"
                android:layout_width="0dp"
                android:layout_weight="1"
                android:layout_height="wrap_content"
                android:text="✅ Grant All Safe"
                android:textSize="12sp"
                android:background="#4CAF50"
                android:textColor="#FFFFFF"
                android:layout_marginEnd="4dp"
                android:minHeight="48dp" />

            <Button
                android:id="@+id/revokeAllButton"
                android:layout_width="0dp"
                android:layout_weight="1"
                android:layout_height="wrap_content"
                android:text="🚫 Revoke All"
                android:textSize="12sp"
                android:background="#F44336"
                android:textColor="#FFFFFF"
                android:layout_marginHorizontal="4dp"
                android:minHeight="48dp" />

            <Button
                android:id="@+id/resetToDefaultsButton"
                android:layout_width="0dp"
                android:layout_weight="1"
                android:layout_height="wrap_content"
                android:text="🔄 Reset"
                android:textSize="12sp"
                android:background="#FF9800"
                android:textColor="#FFFFFF"
                android:layout_marginStart="4dp"
                android:minHeight="48dp" />
        </LinearLayout>

        <!-- Permission Audit Log -->
        <androidx.cardview.widget.CardView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginBottom="16dp"
            app:cardCornerRadius="8dp"
            app:cardElevation="4dp"
            app:cardBackgroundColor="#FFF3E0">

            <LinearLayout
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:orientation="vertical"
                android:padding="16dp">

                <LinearLayout
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:orientation="horizontal"
                    android:gravity="center_vertical"
                    android:layout_marginBottom="12dp">

                    <TextView
                        android:layout_width="0dp"
                        android:layout_weight="1"
                        android:layout_height="wrap_content"
                        android:text="📋 Recent Permission Changes"
                        android:textSize="18sp"
                        android:textStyle="bold"
                        android:textColor="#F57F17" />

                    <Button
                        android:id="@+id/clearAuditLogButton"
                        android:layout_width="wrap_content"
                        android:layout_height="32dp"
                        android:text="🗑️"
                        android:textSize="12sp"
                        android:background="#757575"
                        android:textColor="#FFFFFF"
                        android:minWidth="48dp" />
                </LinearLayout>

                <androidx.recyclerview.widget.RecyclerView
                    android:id="@+id/permissionAuditLogRecyclerView"
                    android:layout_width="match_parent"
                    android:layout_height="150dp"
                    android:background="#FFF8E1"
                    android:padding="8dp" />

                <LinearLayout
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:orientation="horizontal"
                    android:layout_marginTop="8dp">

                    <Button
                        android:id="@+id/exportAuditLogButton"
                        android:layout_width="0dp"
                        android:layout_weight="1"
                        android:layout_height="wrap_content"
                        android:text="📤 Export Log"
                        android:textSize="12sp"
                        android:background="#607D8B"
                        android:textColor="#FFFFFF"
                        android:layout_marginEnd="8dp"
                        android:minHeight="40dp" />

                    <Button
                        android:id="@+id/viewFullLogButton"
                        android:layout_width="0dp"
                        android:layout_weight="1"
                        android:layout_height="wrap_content"
                        android:text="📋 View Full Log"
                        android:textSize="12sp"
                        android:background="#607D8B"
                        android:textColor="#FFFFFF"
                        android:layout_marginStart="8dp"
                        android:minHeight="40dp" />
                </LinearLayout>
            </LinearLayout>
        </androidx.cardview.widget.CardView>

        <!-- Help & Information -->
        <androidx.cardview.widget.CardView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            app:cardCornerRadius="8dp"
            app:cardElevation="4dp"
            app:cardBackgroundColor="#E3F2FD">

            <LinearLayout
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:orientation="vertical"
                android:padding="16dp">

                <TextView
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:text="💡 Permission System Help"
                    android:textSize="18sp"
                    android:textStyle="bold"
                    android:textColor="#1565C0"
                    android:layout_marginBottom="8dp" />

                <TextView
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:text="• Safe permissions: File access, game modification, hooks\n• Dangerous permissions: Network access, native code, system access\n• Sandbox mode isolates plugin execution for security\n• Permission changes are logged for audit purposes\n• Global settings override individual plugin permissions"
                    android:textSize="14sp"
                    android:textColor="#1976D2"
                    android:lineSpacingExtra="4dp" />

                <Button
                    android:id="@+id/viewPermissionDocsButton"
                    android:layout_width="wrap_content"
                    android:layout_height="36dp"
                    android:text="📚 View Documentation"
                    android:textSize="12sp"
                    android:background="#1976D2"
                    android:textColor="#FFFFFF"
                    android:layout_marginTop="8dp"
                    android:minWidth="120dp" />
            </LinearLayout>
        </androidx.cardview.widget.CardView>
    </LinearLayout>
</ScrollView>


/ModLoader/app/src/main/res/menu/log_viewer_menu.xml

<menu xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto">

    <item
        android:id="@+id/action_toggle_filters"
        android:icon="@android:drawable/ic_search_category_default"
        android:title="Toggle Filters"
        app:showAsAction="ifRoom" />

    <item
        android:id="@+id/action_share_logs"
        android:icon="@android:drawable/ic_menu_share"
        android:title="Share Logs"
        app:showAsAction="ifRoom" />

    <item
        android:id="@+id/action_clear_logs"
        android:icon="@android:drawable/ic_menu_delete"
        android:title="Clear Logs"
        app:showAsAction="never" />

    <item
        android:id="@+id/action_settings"
        android:icon="@android:drawable/ic_menu_preferences"
        android:title="Settings"
        app:showAsAction="never" />

</menu>


/ModLoader/app/src/main/res/menu/main_menu.xml

<?xml version="1.0" encoding="utf-8"?>
<menu xmlns:android="http://schemas.android.com/apk/res/android">

    <item
        android:id="@+id/action_log"
        android:title="View Logs"
        android:icon="@android:drawable/ic_menu_info_details"
        android:showAsAction="never" />

    <item
        android:id="@+id/action_about"
        android:title="About"
        android:icon="@android:drawable/ic_menu_help"
        android:showAsAction="never" />

    <item
        android:id="@+id/action_dark_mode"
        android:title="Toggle Dark Mode"
        android:icon="@android:drawable/ic_menu_day"
        android:showAsAction="never" />

    <item
        android:id="@+id/action_export_apk"
        android:title="Export Modified APK"
        android:icon="@android:drawable/ic_menu_save"
        android:showAsAction="never" />

    <item
        android:id="@+id/action_export_logs"
        android:title="Export Logs"
        android:icon="@android:drawable/ic_menu_upload"
        android:showAsAction="never" />
</menu>


/ModLoader/app/src/main/res/mipmap-anydpi-v26/ic_launcher.xml

<?xml version="1.0" encoding="utf-8"?>
<adaptive-icon xmlns:android="http://schemas.android.com/apk/res/android">
    <background android:drawable="@drawable/ic_launcher_background" />
    <foreground android:drawable="@drawable/ic_launcher_foreground" />
</adaptive-icon>


/ModLoader/app/src/main/res/mipmap-anydpi-v26/ic_launcher_round.xml

<?xml version="1.0" encoding="utf-8"?>
<adaptive-icon xmlns:android="http://schemas.android.com/apk/res/android">
    <background android:drawable="@drawable/ic_launcher_background" />
    <foreground android:drawable="@drawable/ic_launcher_foreground" />
</adaptive-icon>


/ModLoader/app/src/main/res/values/colors.xml

<resources>
    <color name="purple_200">#BB86FC</color>
    <color name="purple_500">#6200EE</color>
    <color name="purple_700">#3700B3</color>
    <color name="teal_200">#03DAC5</color>
    <color name="teal_700">#018786</color>
    <color name="black">#000000</color>
    <color name="white">#FFFFFF</color>
    <color name="colorPrimary">#6200EE</color>
</resources>



/ModLoader/app/src/main/res/values/strings.xml

<?xml version="1.0" encoding="utf-8"?>
<resources>
    <string name="app_name">Terraria ML</string>

</resources>


/ModLoader/app/src/main/res/values/themes.xml

<?xml version="1.0" encoding="utf-8"?>
<resources xmlns:tools="http://schemas.android.com/tools">
    <!-- Base application theme (Light) -->
    <style name="Theme.ModLoader" parent="Theme.Material3.DayNight.NoActionBar">
        <item name="colorPrimary">@color/purple_500</item>
        <item name="colorPrimaryVariant">@color/purple_700</item>
        <item name="colorOnPrimary">@color/white</item>
        <item name="colorSecondary">@color/teal_200</item>
        <item name="colorSecondaryVariant">@color/teal_700</item>
        <item name="colorOnSecondary">@color/black</item>
        <item name="android:statusBarColor" tools:targetApi="l">?attr/colorPrimaryVariant</item>
    </style>
</resources>


/ModLoader/app/src/main/res/values-night/colors.xml

<resources>
    <color name="white">#000000</color>
    <color name="black">#FFFFFF</color>
</resources>


/ModLoader/app/src/main/res/values-night/themes.xml

<?xml version="1.0" encoding="utf-8"?>
<resources xmlns:tools="http://schemas.android.com/tools">
    <!-- Night mode theme -->
    <style name="Theme.ModLoader" parent="Theme.Material3.DayNight.NoActionBar">
        <item name="colorPrimary">@color/purple_200</item>
        <item name="colorPrimaryVariant">@color/purple_700</item>
        <item name="colorOnPrimary">@color/black</item>
        <item name="colorSecondary">@color/teal_200</item>
        <item name="colorSecondaryVariant">@color/teal_700</item>
        <item name="colorOnSecondary">@color/white</item>
        <item name="android:statusBarColor" tools:targetApi="l">?attr/colorPrimaryVariant</item>
    </style>
</resources>


/ModLoader/app/src/main/res/xml/backup_rules.xml

<?xml version="1.0" encoding="utf-8"?>
<full-backup-content>
    <!-- Include app-specific files -->
    <include domain="file" path="." />
    <include domain="database" path="." />
    <include domain="sharedpref" path="." />
    <include domain="external" path="Android/data/com.modloader/" />

    <!-- Exclude cache and logs if needed -->
    <exclude domain="cache" path="." />
    <exclude domain="file" path="logs/" />
</full-backup-content>


/ModLoader/app/src/main/res/xml/data_extraction_rules.xml

<?xml version="1.0" encoding="utf-8"?><!--
   Sample data extraction rules file; uncomment and customize as necessary.
   See https://developer.android.com/about/versions/12/backup-restore#xml-changes
   for details.
-->
<data-extraction-rules>
  <cloud-backup>
    <!-- TODO: Use <include> and <exclude> to control what is backed up.
        <include .../>
        <exclude .../>
        -->
  </cloud-backup>
  <!--
    <device-transfer>
        <include .../>
        <exclude .../>
    </device-transfer>
    -->
</data-extraction-rules>


/ModLoader/app/src/main/res/xml/file_paths.xml

<?xml version="1.0" encoding="utf-8"?>
<paths xmlns:android="http://schemas.android.com/apk/res/android">
    <external-files-path
        name="external_files"
        path="." />
</paths>


/ModLoader/app/src/main/res/xml/file_provider_paths.xml

<paths xmlns:android="http://schemas.android.com/tools">
    
    <!-- External storage root (for legacy support) -->
    <external-path 
        name="external_storage_root" 
        path="." />
    
    <!-- App-specific external files directory -->
    <external-files-path 
        name="app_external_files" 
        path="." />
    
    <!-- APK installation directory (FIXED - main issue for APK parsing) -->
    <external-files-path 
        name="apk_install" 
        path="apk_install" />
    
    <!-- Cache directory for temporary files -->
    <external-cache-path 
        name="app_cache" 
        path="." />
    
    <!-- TerrariaLoader main directory -->
    <external-files-path 
        name="terraria_loader" 
        path="TerrariaLoader" />
    
    <!-- Game-specific directories -->
    <external-files-path 
        name="terraria_game" 
        path="TerrariaLoader/com.and.games505.TerrariaPaid" />
    
    <!-- Mod directories -->
    <external-files-path 
        name="dex_mods" 
        path="TerrariaLoader/com.and.games505.TerrariaPaid/Mods/DEX" />
    
    <external-files-path 
        name="dll_mods" 
        path="TerrariaLoader/com.and.games505.TerrariaPaid/Mods/DLL" />
    
    <!-- Log directories -->
    <external-files-path 
        name="app_logs" 
        path="TerrariaLoader/com.and.games505.TerrariaPaid/AppLogs" />
    
    <external-files-path 
        name="game_logs" 
        path="TerrariaLoader/com.and.games505.TerrariaPaid/Logs" />
    
    <!-- Backup directories -->
    <external-files-path 
        name="backups" 
        path="TerrariaLoader/com.and.games505.TerrariaPaid/Backups" />
    
    <!-- Config directories -->
    <external-files-path 
        name="config" 
        path="TerrariaLoader/com.and.games505.TerrariaPaid/Config" />
    
    <!-- MelonLoader directories -->
    <external-files-path 
        name="melonloader" 
        path="TerrariaLoader/com.and.games505.TerrariaPaid/Loaders/MelonLoader" />
    
    <!-- Downloads and exports -->
    <external-files-path 
        name="downloads" 
        path="downloads" />
    
    <external-files-path 
        name="exports" 
        path="exports" />
    
    <!-- Temporary processing directory -->
    <external-files-path 
        name="temp" 
        path="temp" />
    
    <!-- Legacy mod directory (for migration) -->
    <external-files-path 
        name="legacy_mods" 
        path="mods" />

</paths>


/ModLoader/app/src/main/res/xml/paths.xml

<?xml version="1.0" encoding="utf-8"?>
<paths xmlns:android="http://schemas.android.com/apk/res/android">
    <external-files-path
        name="external_files"
        path="." />
</paths>
