/storage/emulated/0/AndroidIDEProjects/ModLoader/ModLoader/app/src/main/res/layout/plugin_hooks_layout.xml

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
            android:text="🔗 Plugin Hook Configuration"
            android:textSize="24sp"
            android:textStyle="bold"
            android:textColor="#2E7D32"
            android:gravity="center"
            android:layout_marginBottom="16dp" />

        <!-- Hook System Status Card -->
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
                    android:text="🔧 Hook System Status"
                    android:textSize="18sp"
                    android:textStyle="bold"
                    android:textColor="#2E7D32"
                    android:layout_marginBottom="8dp" />

                <TextView
                    android:id="@+id/hookStatusText"
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:text="✅ Hook system is active\n🔗 3 hooks registered\n⚡ 12 hook calls processed"
                    android:textSize="14sp"
                    android:textColor="#4CAF50"
                    android:lineSpacingExtra="4dp" />

                <Button
                    android:id="@+id/refreshStatusButton"
                    android:layout_width="wrap_content"
                    android:layout_height="32dp"
                    android:text="🔄 Refresh"
                    android:textSize="12sp"
                    android:background="#4CAF50"
                    android:textColor="#FFFFFF"
                    android:layout_marginTop="8dp"
                    android:minWidth="80dp" />
            </LinearLayout>
        </androidx.cardview.widget.CardView>

        <!-- Available Hooks Card -->
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
                    android:text="📋 Available Hooks"
                    android:textSize="18sp"
                    android:textStyle="bold"
                    android:textColor="#1976D2"
                    android:layout_marginBottom="12dp" />

                <TextView
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:text="These hooks are available for plugins to use:"
                    android:textSize="12sp"
                    android:textColor="#666666"
                    android:layout_marginBottom="8dp" />

                <androidx.recyclerview.widget.RecyclerView
                    android:id="@+id/availableHooksRecyclerView"
                    android:layout_width="match_parent"
                    android:layout_height="200dp"
                    android:background="#FAFAFA"
                    android:padding="8dp" />
            </LinearLayout>
        </androidx.cardview.widget.CardView>

        <!-- Active Hooks Card -->
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
                    android:text="⚡ Active Hooks"
                    android:textSize="18sp"
                    android:textStyle="bold"
                    android:textColor="#FF6F00"
                    android:layout_marginBottom="12dp" />

                <TextView
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:text="Currently installed and active hooks:"
                    android:textSize="12sp"
                    android:textColor="#666666"
                    android:layout_marginBottom="8dp" />

                <androidx.recyclerview.widget.RecyclerView
                    android:id="@+id/activeHooksRecyclerView"
                    android:layout_width="match_parent"
                    android:layout_height="150dp"
                    android:background="#FFF8E1"
                    android:padding="8dp" />
            </LinearLayout>
        </androidx.cardview.widget.CardView>

        <!-- Hook Performance Metrics -->
        <androidx.cardview.widget.CardView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginBottom="16dp"
            app:cardCornerRadius="8dp"
            app:cardElevation="4dp"
            app:cardBackgroundColor="#F3E5F5">

            <LinearLayout
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:orientation="vertical"
                android:padding="16dp">

                <TextView
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:text="📊 Hook Performance"
                    android:textSize="18sp"
                    android:textStyle="bold"
                    android:textColor="#7B1FA2"
                    android:layout_marginBottom="12dp" />

                <LinearLayout
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:orientation="horizontal"
                    android:weightSum="3">

                    <LinearLayout
                        android:layout_width="0dp"
                        android:layout_weight="1"
                        android:layout_height="wrap_content"
                        android:orientation="vertical"
                        android:gravity="center">

                        <TextView
                            android:id="@+id/totalHookCallsText"
                            android:layout_width="wrap_content"
                            android:layout_height="wrap_content"
                            android:text="1,234"
                            android:textSize="20sp"
                            android:textStyle="bold"
                            android:textColor="#7B1FA2" />

                        <TextView
                            android:layout_width="wrap_content"
                            android:layout_height="wrap_content"
                            android:text="Total Calls"
                            android:textSize="12sp"
                            android:textColor="#666666" />
                    </LinearLayout>

                    <LinearLayout
                        android:layout_width="0dp"
                        android:layout_weight="1"
                        android:layout_height="wrap_content"
                        android:orientation="vertical"
                        android:gravity="center">

                        <TextView
                            android:id="@+id/avgExecutionTimeText"
                            android:layout_width="wrap_content"
                            android:layout_height="wrap_content"
                            android:text="2.3ms"
                            android:textSize="20sp"
                            android:textStyle="bold"
                            android:textColor="#7B1FA2" />

                        <TextView
                            android:layout_width="wrap_content"
                            android:layout_height="wrap_content"
                            android:text="Avg Time"
                            android:textSize="12sp"
                            android:textColor="#666666" />
                    </LinearLayout>

                    <LinearLayout
                        android:layout_width="0dp"
                        android:layout_weight="1"
                        android:layout_height="wrap_content"
                        android:orientation="vertical"
                        android:gravity="center">

                        <TextView
                            android:id="@+id/hookErrorsText"
                            android:layout_width="wrap_content"
                            android:layout_height="wrap_content"
                            android:text="0"
                            android:textSize="20sp"
                            android:textStyle="bold"
                            android:textColor="#4CAF50" />

                        <TextView
                            android:layout_width="wrap_content"
                            android:layout_height="wrap_content"
                            android:text="Errors"
                            android:textSize="12sp"
                            android:textColor="#666666" />
                    </LinearLayout>
                </LinearLayout>
            </LinearLayout>
        </androidx.cardview.widget.CardView>

        <!-- Hook Controls -->
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="horizontal"
            android:layout_marginBottom="16dp">

            <Button
                android:id="@+id/refreshHooksButton"
                android:layout_width="0dp"
                android:layout_weight="1"
                android:layout_height="wrap_content"
                android:text="🔄 Refresh Hooks"
                android:textSize="14sp"
                android:background="#2196F3"
                android:textColor="#FFFFFF"
                android:layout_marginEnd="8dp"
                android:minHeight="48dp" />

            <Button
                android:id="@+id/clearHookCacheButton"
                android:layout_width="0dp"
                android:layout_weight="1"
                android:layout_height="wrap_content"
                android:text="🗑️ Clear Cache"
                android:textSize="14sp"
                android:background="#FF9800"
                android:textColor="#FFFFFF"
                android:layout_marginStart="8dp"
                android:minHeight="48dp" />
        </LinearLayout>

        <!-- Hook Documentation -->
        <androidx.cardview.widget.CardView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginBottom="16dp"
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
                    android:text="📖 Hook Documentation"
                    android:textSize="18sp"
                    android:textStyle="bold"
                    android:textColor="#1565C0"
                    android:layout_marginBottom="8dp" />

                <TextView
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:text="• Hooks allow plugins to intercept and modify game events\n• Use registerHook() to install a hook callback\n• Hook callbacks receive parameters and can return modified values\n• Hooks are executed in the order they were registered\n• Failed hooks are automatically disabled to prevent crashes"
                    android:textSize="14sp"
                    android:textColor="#1976D2"
                    android:lineSpacingExtra="4dp" />

                <Button
                    android:id="@+id/viewHookDocsButton"
                    android:layout_width="wrap_content"
                    android:layout_height="36dp"
                    android:text="📚 View Full Documentation"
                    android:textSize="12sp"
                    android:background="#1976D2"
                    android:textColor="#FFFFFF"
                    android:layout_marginTop="8dp"
                    android:minWidth="120dp" />
            </LinearLayout>
        </androidx.cardview.widget.CardView>

        <!-- Debug Section -->
        <androidx.cardview.widget.CardView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
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
                    android:text="🐛 Debug &amp; Testing"
                    android:textSize="18sp"
                    android:textStyle="bold"
                    android:textColor="#C62828"
                    android:layout_marginBottom="12dp" />

                <CheckBox
                    android:id="@+id/enableHookDebuggingCheckbox"
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:text="Enable hook debugging (logs all hook calls)"
                    android:textSize="14sp"
                    android:textColor="#D32F2F"
                    android:layout_marginBottom="8dp" />

                <LinearLayout
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:orientation="horizontal">

                    <Button
                        android:id="@+id/testHooksButton"
                        android:layout_width="0dp"
                        android:layout_weight="1"
                        android:layout_height="wrap_content"
                        android:text="🧪 Test Hooks"
                        android:textSize="12sp"
                        android:background="#D32F2F"
                        android:textColor="#FFFFFF"
                        android:layout_marginEnd="8dp"
                        android:minHeight="40dp" />

                    <Button
                        android:id="@+id/exportHookLogsButton"
                        android:layout_width="0dp"
                        android:layout_weight="1"
                        android:layout_height="wrap_content"
                        android:text="📤 Export Logs"
                        android:textSize="12sp"
                        android:background="#757575"
                        android:textColor="#FFFFFF"
                        android:layout_marginStart="8dp"
                        android:minHeight="40dp" />
                </LinearLayout>
            </LinearLayout>
        </androidx.cardview.widget.CardView>
    </LinearLayout>
</ScrollView>

/storage/emulated/0/AndroidIDEProjects/ModLoader/ModLoader/app/src/main/res/layout/plugin_permissions_layout.xml

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

/storage/emulated/0/AndroidIDEProjects/ModLoader/ModLoader/app/src/main/res/menu/log_viewer_menu.xml

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

/storage/emulated/0/AndroidIDEProjects/ModLoader/ModLoader/app/src/main/res/menu/main_menu.xml

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

/storage/emulated/0/AndroidIDEProjects/ModLoader/ModLoader/app/src/main/res/mipmap-anydpi-v26/ic_launcher.xml

<?xml version="1.0" encoding="utf-8"?>
<adaptive-icon xmlns:android="http://schemas.android.com/apk/res/android">
    <background android:drawable="@drawable/ic_launcher_background" />
    <foreground android:drawable="@drawable/ic_launcher_foreground" />
</adaptive-icon>

/storage/emulated/0/AndroidIDEProjects/ModLoader/ModLoader/app/src/main/res/mipmap-anydpi-v26/ic_launcher_round.xml

<?xml version="1.0" encoding="utf-8"?>
<adaptive-icon xmlns:android="http://schemas.android.com/apk/res/android">
    <background android:drawable="@drawable/ic_launcher_background" />
    <foreground android:drawable="@drawable/ic_launcher_foreground" />
</adaptive-icon>

/storage/emulated/0/AndroidIDEProjects/ModLoader/ModLoader/app/src/main/res/values/colors.xml

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


/storage/emulated/0/AndroidIDEProjects/ModLoader/ModLoader/app/src/main/res/values/strings.xml

<resources>
    <!-- App Name -->
    <string name="app_name">Mod Loader</string>
    
    <!-- Main Activity -->
    <string name="main_title">Mod Loader - Main Menu</string>
    <string name="universal_mode">Universal Mode</string>
    <string name="specific_mode">Specific Mode</string>
    <string name="plugin_management">Plugin Management</string>
    
    <!-- Existing Strings -->
    <string name="terraria_ml">Terraria ML</string>
    <string name="about_title">About Mod Loader</string>
    <string name="settings_title">Settings</string>
    
    <!-- NEW: Plugin System Strings -->
    <string name="plugin_system_title">Plugin System</string>
    <string name="plugin_management_title">Plugin Management</string>
    <string name="plugin_install_title">Install Plugin</string>
    <string name="plugin_config_title">Plugin Configuration</string>
    
    <!-- Plugin Management -->
    <string name="plugin_manager">Plugin Manager</string>
    <string name="plugin_install">Install Plugin</string>
    <string name="plugin_config">Plugin Config</string>
    <string name="plugin_enable">Enable</string>
    <string name="plugin_disable">Disable</string>
    <string name="plugin_remove">Remove</string>
    <string name="plugin_update">Update</string>
    <string name="plugin_reload">Reload</string>
    <string name="plugin_restart">Restart</string>
    
    <!-- Plugin Installation -->
    <string name="plugin_install_from_file">Install from File</string>
    <string name="plugin_install_from_url">Install from URL</string>
    <string name="plugin_install_success">Plugin installed successfully</string>
    <string name="plugin_install_failed">Plugin installation failed</string>
    <string name="plugin_install_progress">Installing plugin…</string>
    <string name="plugin_select_file">Select Plugin File</string>
    <string name="plugin_enter_url">Enter Plugin URL</string>
    <string name="plugin_download_progress">Downloading plugin…</string>
    
    <!-- Plugin Configuration -->
    <string name="plugin_config_general">General Settings</string>
    <string name="plugin_config_permissions">Permissions</string>
    <string name="plugin_config_storage">Storage Settings</string>
    <string name="plugin_config_network">Network Settings</string>
    <string name="plugin_config_hooks">Hook Configuration</string>
    <string name="plugin_config_advanced">Advanced Settings</string>
    <string name="plugin_config_save">Save Configuration</string>
    <string name="plugin_config_reset">Reset to Defaults</string>
    
    <!-- Plugin Status -->
    <string name="plugin_status_enabled">Enabled</string>
    <string name="plugin_status_disabled">Disabled</string>
    <string name="plugin_status_loading">Loading…</string>
    <string name="plugin_status_error">Error</string>
    <string name="plugin_status_updating">Updating…</string>
    <string name="plugin_status_inactive">Inactive</string>
    <string name="plugin_status_active">Active</string>
    <string name="plugin_status_crashed">Crashed</string>
    
    <!-- Plugin Types -->
    <string name="plugin_type_theme">Theme Plugin</string>
    <string name="plugin_type_modification">Modification Plugin</string>
    <string name="plugin_type_utility">Utility Plugin</string>
    <string name="plugin_type_game_mod">Game Mod Plugin</string>
    <string name="plugin_type_ui_extension">UI Extension</string>
    <string name="plugin_type_unknown">Unknown Plugin</string>
    
    <!-- Plugin Permissions (NEW) -->
    <string name="permission_plugin_api_label">Plugin API Access</string>
    <string name="permission_plugin_api_desc">Allows plugin to access the ModLoader plugin API</string>
    
    <string name="permission_plugin_install_label">Install Plugins</string>
    <string name="permission_plugin_install_desc">Allows installation of new plugins</string>
    
    <string name="permission_plugin_manage_label">Manage Plugins</string>
    <string name="permission_plugin_manage_desc">Allows management of existing plugins</string>
    
    <string name="permission_file_system">File System Access</string>
    <string name="permission_network_access">Network Access</string>
    <string name="permission_game_modification">Game Modification</string>
    <string name="permission_hook_installation">Hook Installation</string>
    <string name="permission_native_code">Native Code Execution</string>
    <string name="permission_system_access">System Access</string>
    
    <!-- Plugin Service -->
    <string name="plugin_service_description">ModLoader Plugin Service - Manages plugin lifecycle and execution</string>
    <string name="plugin_service_starting">Starting Plugin Service</string>
    <string name="plugin_service_stopping">Stopping Plugin Service</string>
    <string name="plugin_service_running">Plugin Service Running</string>
    <string name="plugin_service_stopped">Plugin Service Stopped</string>
    
    <!-- Plugin Security -->
    <string name="plugin_security_title">Plugin Security</string>
    <string name="plugin_sandbox_enabled">Sandbox Mode Enabled</string>
    <string name="plugin_sandbox_disabled">Sandbox Mode Disabled</string>
    <string name="plugin_permission_granted">Permission Granted</string>
    <string name="plugin_permission_denied">Permission Denied</string>
    <string name="plugin_permission_request">Permission Request</string>
    <string name="plugin_security_check">Security Check</string>
    <string name="plugin_security_warning">Security Warning</string>
    
    <!-- Plugin Validation -->
    <string name="plugin_validation_success">Plugin validation successful</string>
    <string name="plugin_validation_failed">Plugin validation failed</string>
    <string name="plugin_validation_warning">Plugin validation warning</string>
    <string name="plugin_signature_valid">Plugin signature is valid</string>
    <string name="plugin_signature_invalid">Plugin signature is invalid</string>
    <string name="plugin_checksum_valid">Plugin checksum is valid</string>
    <string name="plugin_checksum_invalid">Plugin checksum is invalid</string>
    
    <!-- Plugin Storage -->
    <string name="plugin_storage_title">Plugin Storage</string>
    <string name="plugin_storage_usage">Storage Usage</string>
    <string name="plugin_storage_clear">Clear Storage</string>
    <string name="plugin_storage_backup">Backup Storage</string>
    <string name="plugin_storage_restore">Restore Storage</string>
    <string name="plugin_storage_export">Export Storage</string>
    <string name="plugin_storage_import">Import Storage</string>
    
    <!-- Plugin Hooks -->
    <string name="plugin_hooks_title">Plugin Hooks</string>
    <string name="plugin_hook_installed">Hook Installed</string>
    <string name="plugin_hook_removed">Hook Removed</string>
    <string name="plugin_hook_active">Hook Active</string>
    <string name="plugin_hook_inactive">Hook Inactive</string>
    <string name="plugin_hook_error">Hook Error</string>
    <string name="plugin_hooks_count">Active Hooks: %d</string>
    
    <!-- Plugin Context -->
    <string name="plugin_context_title">Plugin Context</string>
    <string name="plugin_context_app">App Context</string>
    <string name="plugin_context_game">Game Context</string>
    <string name="plugin_context_system">System Context</string>
    <string name="plugin_context_isolated">Isolated Context</string>
    
    <!-- Plugin Registry -->
    <string name="plugin_registry_title">Plugin Registry</string>
    <string name="plugin_registry_loaded">Plugin Registered</string>
    <string name="plugin_registry_unloaded">Plugin Unregistered</string>
    <string name="plugin_registry_error">Registry Error</string>
    <string name="plugin_registry_count">Registered Plugins: %d</string>
    
    <!-- Plugin Loader -->
    <string name="plugin_loader_title">Plugin Loader</string>
    <string name="plugin_loader_loading">Loading Plugins…</string>
    <string name="plugin_loader_complete">Plugin Loading Complete</string>
    <string name="plugin_loader_failed">Plugin Loading Failed</string>
    <string name="plugin_loader_progress">Loading: %s</string>
    
    <!-- Plugin API -->
    <string name="plugin_api_title">Plugin API</string>
    <string name="plugin_api_version">API Version: %s</string>
    <string name="plugin_api_compatible">API Compatible</string>
    <string name="plugin_api_incompatible">API Incompatible</string>
    
    <!-- Plugin Dialogs -->
    <string name="dialog_plugin_install_title">Install Plugin</string>
    <string name="dialog_plugin_install_message">Do you want to install this plugin?</string>
    <string name="dialog_plugin_remove_title">Remove Plugin</string>
    <string name="dialog_plugin_remove_message">Are you sure you want to remove this plugin?</string>
    <string name="dialog_plugin_enable_title">Enable Plugin</string>
    <string name="dialog_plugin_enable_message">Do you want to enable this plugin?</string>
    <string name="dialog_plugin_disable_title">Disable Plugin</string>
    <string name="dialog_plugin_disable_message">Do you want to disable this plugin?</string>
    <string name="dialog_plugin_update_title">Update Plugin</string>
    <string name="dialog_plugin_update_message">A new version is available. Update now?</string>
    <string name="dialog_plugin_permission_title">Plugin Permission Request</string>
    <string name="dialog_plugin_permission_message">This plugin requests the following permissions:</string>
    
    <!-- Plugin Error Messages -->
    <string name="error_plugin_not_found">Plugin not found</string>
    <string name="error_plugin_corrupted">Plugin file is corrupted</string>
    <string name="error_plugin_incompatible">Plugin is not compatible</string>
    <string name="error_plugin_duplicate">Plugin already installed</string>
    <string name="error_plugin_load_failed">Failed to load plugin</string>
    <string name="error_plugin_init_failed">Failed to initialize plugin</string>
    <string name="error_plugin_permission_denied">Plugin permission denied</string>
    <string name="error_plugin_security_violation">Plugin security violation</string>
    
    <!-- Plugin Success Messages -->
    <string name="success_plugin_installed">Plugin installed successfully</string>
    <string name="success_plugin_removed">Plugin removed successfully</string>
    <string name="success_plugin_enabled">Plugin enabled successfully</string>
    <string name="success_plugin_disabled">Plugin disabled successfully</string>
    <string name="success_plugin_updated">Plugin updated successfully</string>
    <string name="success_plugin_configured">Plugin configured successfully</string>
    
    <!-- Plugin File Types -->
    <string name="plugin_file_jar">JAR Plugin File</string>
    <string name="plugin_file_dex">DEX Plugin File</string>
    <string name="plugin_file_zip">ZIP Plugin Package</string>
    <string name="plugin_file_unknown">Unknown Plugin File</string>
    
    <!-- Plugin Categories -->
    <string name="category_all_plugins">All Plugins</string>
    <string name="category_enabled_plugins">Enabled Plugins</string>
    <string name="category_disabled_plugins">Disabled Plugins</string>
    <string name="category_system_plugins">System Plugins</string>
    <string name="category_user_plugins">User Plugins</string>
    <string name="category_theme_plugins">Theme Plugins</string>
    <string name="category_mod_plugins">Mod Plugins</string>
    <string name="category_utility_plugins">Utility Plugins</string>
    
    <!-- Plugin Actions -->
    <string name="action_install_plugin">Install Plugin</string>
    <string name="action_enable_plugin">Enable Plugin</string>
    <string name="action_disable_plugin">Disable Plugin</string>
    <string name="action_configure_plugin">Configure Plugin</string>
    <string name="action_update_plugin">Update Plugin</string>
    <string name="action_remove_plugin">Remove Plugin</string>
    <string name="action_reload_plugin">Reload Plugin</string>
    <string name="action_restart_plugin">Restart Plugin</string>
    
    <!-- Plugin Menu Items -->
    <string name="menu_plugin_info">Plugin Info</string>
    <string name="menu_plugin_settings">Plugin Settings</string>
    <string name="menu_plugin_permissions">Plugin Permissions</string>
    <string name="menu_plugin_storage">Plugin Storage</string>
    <string name="menu_plugin_logs">Plugin Logs</string>
    <string name="menu_plugin_about">About Plugin</string>
    
    <!-- Plugin Information -->
    <string name="plugin_info_name">Name:</string>
    <string name="plugin_info_version">Version:</string>
    <string name="plugin_info_author">Author:</string>
    <string name="plugin_info_description">Description:</string>
    <string name="plugin_info_size">Size:</string>
    <string name="plugin_info_install_date">Installed:</string>
    <string name="plugin_info_last_used">Last Used:</string>
    <string name="plugin_info_api_version">API Version:</string>
    
    <!-- Plugin Statistics -->
    <string name="stats_total_plugins">Total Plugins: %d</string>
    <string name="stats_enabled_plugins">Enabled: %d</string>
    <string name="stats_disabled_plugins">Disabled: %d</string>
    <string name="stats_system_plugins">System: %d</string>
    <string name="stats_user_plugins">User: %d</string>
    <string name="stats_plugin_storage_usage">Storage Used: %s</string>
    
    <!-- Plugin Tips -->
    <string name="tip_plugin_sandbox">Enable sandbox mode for better security</string>
    <string name="tip_plugin_permissions">Review plugin permissions carefully</string>
    <string name="tip_plugin_backup">Backup your plugins before updates</string>
    <string name="tip_plugin_logs">Check plugin logs for troubleshooting</string>
    
    <!-- Common Actions -->
    <string name="action_ok">OK</string>
    <string name="action_cancel">Cancel</string>
    <string name="action_yes">Yes</string>
    <string name="action_no">No</string>
    <string name="action_apply">Apply</string>
    <string name="action_save">Save</string>
    <string name="action_reset">Reset</string>
    <string name="action_close">Close</string>
    <string name="action_refresh">Refresh</string>
    <string name="action_select">Select</string>
    <string name="action_browse">Browse</string>
    <string name="action_download">Download</string>
    <string name="action_upload">Upload</string>
    <string name="action_export">Export</string>
    <string name="action_import">Import</string>
    <string name="action_backup">Backup</string>
    <string name="action_restore">Restore</string>
    <string name="action_delete">Delete</string>
    <string name="action_edit">Edit</string>
    <string name="action_view">View</string>
    <string name="action_share">Share</string>
    
</resources>

/storage/emulated/0/AndroidIDEProjects/ModLoader/ModLoader/app/src/main/res/values/themes.xml

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

/storage/emulated/0/AndroidIDEProjects/ModLoader/ModLoader/app/src/main/res/values-night/colors.xml

<resources>
    <color name="white">#000000</color>
    <color name="black">#FFFFFF</color>
</resources>

/storage/emulated/0/AndroidIDEProjects/ModLoader/ModLoader/app/src/main/res/values-night/themes.xml

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

/storage/emulated/0/AndroidIDEProjects/ModLoader/ModLoader/app/src/main/res/xml/backup_rules.xml

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

/storage/emulated/0/AndroidIDEProjects/ModLoader/ModLoader/app/src/main/res/xml/data_extraction_rules.xml

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

/storage/emulated/0/AndroidIDEProjects/ModLoader/ModLoader/app/src/main/res/xml/file_paths.xml

<?xml version="1.0" encoding="utf-8"?>
<paths xmlns:android="http://schemas.android.com/apk/res/android">
    <external-files-path
        name="external_files"
        path="." />
</paths>

/storage/emulated/0/AndroidIDEProjects/ModLoader/ModLoader/app/src/main/res/xml/file_provider_paths.xml

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
    
    <!-- ModLoader main directory -->
    <external-files-path 
        name="terraria_loader" 
        path="ModLoader" />
    
    <!-- Game-specific directories -->
    <external-files-path 
        name="terraria_game" 
        path="ModLoader/com.and.games505.TerrariaPaid" />
    
    <!-- Mod directories -->
    <external-files-path 
        name="dex_mods" 
        path="ModLoader/com.and.games505.TerrariaPaid/Mods/DEX" />
    
    <external-files-path 
        name="dll_mods" 
        path="ModLoader/com.and.games505.TerrariaPaid/Mods/DLL" />
    
    <!-- Log directories -->
    <external-files-path 
        name="app_logs" 
        path="ModLoader/com.and.games505.TerrariaPaid/AppLogs" />
    
    <external-files-path 
        name="game_logs" 
        path="ModLoader/com.and.games505.TerrariaPaid/Logs" />
    
    <!-- Backup directories -->
    <external-files-path 
        name="backups" 
        path="ModLoader/com.and.games505.TerrariaPaid/Backups" />
    
    <!-- Config directories -->
    <external-files-path 
        name="config" 
        path="ModLoader/com.and.games505.TerrariaPaid/Config" />
    
    <!-- MelonLoader directories -->
    <external-files-path 
        name="melonloader" 
        path="ModLoader/com.and.games505.TerrariaPaid/Loaders/MelonLoader" />
    
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

/storage/emulated/0/AndroidIDEProjects/ModLoader/ModLoader/app/src/main/res/xml/paths.xml

<?xml version="1.0" encoding="utf-8"?>
<paths xmlns:android="http://schemas.android.com/apk/res/android">
    <external-files-path
        name="external_files"
        path="." />
</paths>

