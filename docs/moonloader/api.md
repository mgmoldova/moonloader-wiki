# Справочник API MoonLoader

Здесь перечислены все глобальные функции, события, переменные и константы, которые MoonLoader добавляет для Lua-скриптов.

!!! tip "Фильтрация и поиск"
    Вы можете воспользоваться глобальным поиском в правом верхнем углу сайта, чтобы мгновенно найти нужную функцию по её названию или возвращаемому типу. Для категорий используйте теги: `функции`, `события`, `переменные`, `константы`, `классы`.

Информация о типах параметров и возвращаемых значений подробно расписана на странице [Типы данных MoonLoader](data-types.md).

!!! warning "Отсутствующие описания"
    Если ссылка на функцию ведет на несуществующую страницу (выделена красным), это означает, что статья для неё ещё не написана. В таком случае синтаксис и особенности работы функции рекомендуется искать в документации **Sanny Builder**.

---

## Глобальные функции (Lua)

| Функции (Lua) |
| :--- |
| [`bool result = isCursorActive()`](lua/isCursorActive.md) |
| [`table pickups = getAllPickups()`](lua/getAllPickups.md) |
| [`int handle = getPickupPointerHandle(Pickup pickup)`](lua/getPickupPointerHandle.md) |
| [`int pointer = getPickupPointer(Pickup pickup)`](lua/getPickupPointer.md) |
| [`int type = getPickupType(Pickup pickup)`](lua/getPickupType.md) |
| [`int model = getPickupModel(Pickup pickup)`](lua/getPickupModel.md) |
| [`float x, float y, float z, float w = getObjectQuaternion(Object object)`](lua/getObjectQuaternion.md) |
| [`setObjectQuaternion(Object object, float x, float y, float z, float w)`](lua/setObjectQuaternion.md) |
| [`float x, float y, float z, float w = getVehicleQuaternion(Vehicle car)`](lua/getVehicleQuaternion.md) |
| [`setVehicleQuaternion(Vehicle car, float x, float y, float z, float w)`](lua/setVehicleQuaternion.md) |
| [`float x, float y, float z, float w = getCharQuaternion(Ped ped)`](lua/getCharQuaternion.md) |
| [`setCharQuaternion(Ped ped, float x, float y, float z, float w)`](lua/setCharQuaternion.md) |
| [`AudioStream handle = loadAudioStream(zstring audio)`](lua/loadAudioStream.md) |
| [`setAudioStreamState(AudioStream handle, int state)`](lua/setAudioStreamState.md) |
| [`releaseAudioStream(AudioStream handle)`](lua/releaseAudioStream.md) |
| [`double length = getAudioStreamLength(AudioStream handle)`](lua/getAudioStreamLength.md) |
| [`int state = getAudioStreamState(AudioStream handle)`](lua/getAudioStreamState.md) |
| [`float volume = getAudioStreamVolume(AudioStream audio)`](lua/getAudioStreamVolume.md) |
| [`setAudioStreamVolume(AudioStream audio, float volume)`](lua/setAudioStreamVolume.md) |
| [`setAudioStreamLooped(AudioStream audio, bool loop)`](lua/setAudioStreamLooped.md) |
| [`AudioStream handle = load3dAudioStream(zstring audio)`](lua/load3dAudioStream.md) |
| [`setPlay3dAudioStreamAtCoordinates(AudioStream handle, float posX, float posY, float posZ)`](lua/setPlay3dAudioStreamAtCoordinates.md) |
| [`setPlay3dAudioStreamAtObject(AudioStream audio, Object object)`](lua/setPlay3dAudioStreamAtObject.md) |
| [`setPlay3dAudioStreamAtChar(AudioStream audio, Ped ped)`](lua/setPlay3dAudioStreamAtChar.md) |
| [`setPlay3dAudioStreamAtCar(AudioStream audio, Vehicle car)`](lua/setPlay3dAudioStreamAtCar.md) |
| [`AudioStream handle = loadAudioStreamFromMemory(uint address, uint size)`](lua/loadAudioStreamFromMemory.md) |
| [`AudioStream handle = load3dAudioStreamFromMemory(uint address, uint size)`](lua/load3dAudioStreamFromMemory.md) |
| [`renderDrawLine(float pos1X, float pos1Y, float pos2X, float pos2Y, float width, uint color)`](lua/renderDrawLine.md) |
| [`renderDrawBox(float posX, float posY, float sizeX, float sizeY, uint color)`](lua/renderDrawBox.md) |
| [`renderDrawBoxWithBorder(float posX, float posY, float sizeX, float sizeY, uint color, float bsize, uint bcolor)`](lua/renderDrawBoxWithBorder.md) |
| [`float length = renderGetFontDrawTextLength(DxFont font, zstring text, [bool ignoreColorTags=false])`](lua/renderGetFontDrawTextLength.md) |
| [`float height = renderGetFontDrawHeight(DxFont font)`](lua/renderGetFontDrawHeight.md) |
| [`uint index = renderGetFontCharIndexAt(DxFont font, string text, float x, [bool ignoreColorTags=false])`](lua/renderGetFontCharIndexAt.md) |
| [`float width = renderGetFontCharWidth(DxFont font, string/uint char)`](lua/renderGetFontCharWidth.md) |
| [`DxFont font = renderCreateFont(zstring font, int height, uint flags, [uint charset])`](lua/renderCreateFont.md) |
| [`renderReleaseFont(DxFont font)`](lua/renderReleaseFont.md) |
| [`renderFontDrawText(DxFont font, zstring text, float posX, float posY, uint color, [bool ignoreColorTags=false])`](lua/renderFontDrawText.md) |
| [`renderDrawPolygon(float posX, float posY, float sizeX, float sizeY, int corners, float rotation, uint color)`](lua/renderDrawPolygon.md) |
| [`DxTexture texture = renderLoadTextureFromFile(zstring file)`](lua/renderLoadTextureFromFile.md) |
| [`renderReleaseTexture(DxTexture texture)`](lua/renderReleaseTexture.md) |
| [`renderDrawTexture(DxTexture texture, float posX, float posY, float sizeX, float sizeY, float rotation, uint color)`](lua/renderDrawTexture.md) |
| [`renderBegin(int type)`](lua/renderBegin.md) |
| [`renderEnd()`](lua/renderEnd.md) |
| [`renderColor(uint color)`](lua/renderColor.md) |
| [`renderVertex(float vX, float vY)`](lua/renderVertex.md) |
| [`renderSetTexCoord(float posX, float posY)`](lua/renderSetTexCoord.md) |
| [`renderBindTexture(DxTexture texture)`](lua/renderBindTexture.md) |
| [`uint struct = renderGetTextureStruct(DxTexture texture)`](lua/renderGetTextureStruct.md) |
| [`uint sprite = renderGetTextureSprite(DxTexture texture)`](lua/renderGetTextureSprite.md) |
| [`uint sizeX, uint sizeY = renderGetTextureSize(DxTexture texture)`](lua/renderGetTextureSize.md) |
| [`renderSetRenderState(int state, uint value)`](lua/renderSetRenderState.md) |
| [`DxTexture texture = renderLoadTextureFromFileInMemory(uint pointer, uint size)`](lua/renderLoadTextureFromFileInMemory.md) |
| [`script_version_number(int version)`](lua/script_version_number.md) |
| [`script_version(string version)`](lua/script_version.md) |
| [`script_name(string name)`](lua/script_name.md) |
| [`script_description(string description)`](lua/script_description.md) |
| [`script_authors(string author, ...)`](lua/script_authors.md) |
| [`script_author(string author)`](lua/script_author.md) |
| [`script_dependencies(string name, ...)`](lua/script_dependencies.md) |
| [`script_moonloader(int version)`](lua/script_moonloader.md) |
| [`LuaScript s = thisScript()`](lua/thisScript.md) |
| [`wait(int time)`](lua/wait.md) |
| [`print(any value, ...)`](lua/print.md) |
| [`int value = getGameGlobal(int index)`](lua/getGameGlobal.md) |
| [`setGameGlobal(int index, int value)`](lua/setGameGlobal.md) |
| [`uint ptr = getGameGlobalPtr(int index)`](lua/getGameGlobalPtr.md) |
| [`bool loaded = isSampfuncsLoaded()`](lua/isSampfuncsLoaded.md) |
| [`bool loaded = isCleoLoaded()`](lua/isCleoLoaded.md) |
| [`bool loaded = isSampLoaded()`](lua/isSampLoaded.md) |
| [`bool state = isKeyDown(int keyId)`](lua/isKeyDown.md) |
| [`reloadScripts()`](lua/reloadScripts.md) |
| [`bool status = isOpcodesAvailable()`](lua/isOpcodesAvailable.md) |
| [`int i = representFloatAsInt(float f)`](lua/representFloatAsInt.md) |
| [`float i = representIntAsFloat(int i)`](lua/representIntAsFloat.md) |
| [`setGxtEntry(string key, string text)`](lua/setGxtEntry.md) |
| [`string key = setFreeGxtEntry(string text)`](lua/setFreeGxtEntry.md) |
| [`string key = getFreeGxtKey()`](lua/getFreeGxtKey.md) |
| [`string text = getGxtText(string key)`](lua/getGxtText.md) |
| [`clearGxtEntry(string key)`](lua/clearGxtEntry.md) |
| [`bool active = isPauseMenuActive()`](lua/isPauseMenuActive.md) |
| [`bool foreground = isGameWindowForeground()`](lua/isGameWindowForeground.md) |
| [`int major, int minor, int majorRev, int minorRev, int game, int region, bool steam, bool cracked = getGameVersion()`](lua/getGameVersion.md) |
| [`int version = getMoonloaderVersion()`](lua/getMoonloaderVersion.md) |
| [`double time = localClock()`](lua/localClock.md) |
| [`freeTextures()`](lua/freeTextures.md) |
| [`string path = getWorkingDirectory()`](lua/getWorkingDirectory.md) |
| [`string path = getGameDirectory()`](lua/getGameDirectory.md) |
| [`useRenderCommands(bool enable)`](lua/useRenderCommands.md) |
| [`writeMemory(uint address, uint size, int value, bool virtualProtect)`](lua/writeMemory.md) |
| [`int value = readMemory(uint address, uint size, bool virtualProtect)`](lua/readMemory.md) |
| [`bool result, uint handle = loadDynamicLibrary(string library)`](lua/loadDynamicLibrary.md) |
| [`freeDynamicLibrary(uint handle)`](lua/freeDynamicLibrary.md) |
| [`bool result, uint proc = getDynamicLibraryProcedure(string proc, uint handle)`](lua/getDynamicLibraryProcedure.md) |
| [`bool result = doesFileExist(string file)`](lua/doesFileExist.md) |
| [`bool result = doesDirectoryExist(string directory)`](lua/doesDirectoryExist.md) |
| [`bool result = createDirectory(string directory)`](lua/createDirectory.md) |
| [`float val = popFloat()`](lua/popFloat.md) |
| [`bool result = isGameVersionOriginal()`](lua/isGameVersionOriginal.md) |
| [`uint memory = allocateMemory(uint size)`](lua/allocateMemory.md) |
| [`freeMemory(uint memory)`](lua/freeMemory.md) |
| [`Filesearch handle, string name = findFirstFile(string mask)`](lua/findFirstFile.md) |
| [`string file = findNextFile(Filesearch handle)`](lua/findNextFile.md) |
| [`findClose(Filesearch handle)`](lua/findClose.md) |
| [`bool result, Ped ped = findAllRandomCharsInSphere(float posX, float posY, float posZ, float radius, bool findNext, bool skipDead)`](lua/findAllRandomCharsInSphere.md) |
| [`bool result, Vehicle car = findAllRandomVehiclesInSphere(float posX, float posY, float posZ, float radius, bool findNext, bool skipWrecked)`](lua/findAllRandomVehiclesInSphere.md) |
| [`bool result, Object object = findAllRandomObjectsInSphere(float posX, float posY, float posZ, float radius, bool findNext)`](lua/findAllRandomObjectsInSphere.md) |
| [`uint ptr = getCharPointer(Ped ped)`](lua/getCharPointer.md) |
| [`uint ptr = getCarPointer(Vehicle car)`](lua/getCarPointer.md) |
| [`uint struct = getObjectPointer(Object object)`](lua/getObjectPointer.md) |
| [`int returnValue = callFunction(uint address, int params, int pop, ...)`](lua/callFunction.md) |
| [`int returnValue = callMethod(uint address, int struct, int params, int pop, ...)`](lua/callMethod.md) |
| [`Vehicle car, Ped ped = storeClosestEntities(Ped ped)`](lua/storeClosestEntities.md) |
| [`switchCarEngine(Vehicle car, bool state)`](lua/switchCarEngine.md) |
| [`bool result, float posX, float posY, float posZ = getTargetBlipCoordinates()`](lua/getTargetBlipCoordinates.md) |
| [`int gears = getCarNumberOfGears(Vehicle car)`](lua/getCarNumberOfGears.md) |
| [`int gear = getCarCurrentGear(Vehicle car)`](lua/getCarCurrentGear.md) |
| [`bool state = isCarSirenOn(Vehicle car)`](lua/isCarSirenOn.md) |
| [`bool state = isCarEngineOn(Vehicle car)`](lua/isCarEngineOn.md) |
| [`printHelpString(string text)`](lua/printHelpString.md) |
| [`printStyledString(string text, int time, int style)`](lua/printStyledString.md) |
| [`printString(string text, int time)`](lua/printString.md) |
| [`printStringNow(string text, int time)`](lua/printStringNow.md) |
| [`bool result, Ped ped = getCharPlayerIsTargeting(Player player)`](lua/getCharPlayerIsTargeting.md) |
| [`GxtString name = getNameOfVehicleModel(Model modelId)`](lua/getNameOfVehicleModel.md) |
| [`bool result = testCheat(string text)`](lua/testCheat.md) |
| [`bool result = spawnVehicleByCheating(Model modelId)`](lua/spawnVehicleByCheating.md) |
| [`Ped handle = getCharPointerHandle(uint ptr)`](lua/getCharPointerHandle.md) |
| [`Vehicle handle = getVehiclePointerHandle(uint ptr)`](lua/getVehiclePointerHandle.md) |
| [`Object handle = getObjectPointerHandle(uint ptr)`](lua/getObjectPointerHandle.md) |
| [`bool result, table colPoint = processLineOfSight(float originX, float originY, float originZ, float targetX, float targetY, float targetZ, [bool checkSolid=true], [bool car=false], [bool ped=false], [bool object=false], [bool particle=false], [bool seeThrough=false], [bool ignoreSomeObjects=false], [bool shootThrough=false])`](lua/processLineOfSight.md) |
| [`bool result = setClipboardText(string text)`](lua/setClipboardText.md) |
| [`string text = getClipboardText()`](lua/getClipboardText.md) |
| [`int value = getStructElement(uint struct, int offset, uint size, [bool unprotect=false])`](lua/getStructElement.md) |
| [`setStructElement(uint struct, int offset, uint size, int value, [bool unprotect=false])`](lua/setStructElement.md) |
| [`float w, float x, float y, float z = convertMatrixToQuaternion(float rightX, float rightY, float rightZ, float frontX, float frontY, float frontZ, float upX, float upY, float upZ)`](lua/convertMatrixToQuaternion.md) |
| [`float rightX, float rightY, float rightZ, float frontX, float frontY, float frontZ, float upX, float upY, float upZ = convertQuaternionToMatrix(float w, float x, float y, float z)`](lua/convertQuaternionToMatrix.md) |
| [`float wposX, float wposY = convert3DCoordsToScreen(float posX, float posY, float posZ)`](lua/convert3DCoordsToScreen.md) |
| [`setGameKeyState(int key, int state)`](lua/setGameKeyState.md) |
| [`int posX, int posY = getCursorPos()`](lua/getCursorPos.md) |
| [`float gposX, float gposY = convertWindowScreenCoordsToGameScreenCoords(float wposX, float wposY)`](lua/convertWindowScreenCoordsToGameScreenCoords.md) |
| [`float wposX, float wposY = convertGameScreenCoordsToWindowScreenCoords(float gposX, float gposY)`](lua/convertGameScreenCoordsToWindowScreenCoords.md) |
| [`float posX, float posY, float posZ = convertScreenCoordsToWorld3D(float posX, float posY, float depth)`](lua/convertScreenCoordsToWorld3D.md) |
| [`uint handle = getModuleHandle(string module)`](lua/getModuleHandle.md) |
| [`uint address = getModuleProcAddress(string module, string proc)`](lua/getModuleProcAddress.md) |
| [`setVirtualKeyDown(int vkey, bool down)`](lua/setVirtualKeyDown.md) |
| [`setCharKeyDown(int ckey, bool down)`](lua/setCharKeyDown.md) |
| [`int index = downloadUrlToFile(string url, string file, function statusCallback)`](lua/downloadUrlToFile.md) |
| [`bool state = isKeyJustPressed(int key)`](lua/isKeyJustPressed.md) |
| [`bool result, float x, float y, float z, float w, float h = convert3DCoordsToScreenEx(float posX, float posY, float posZ, [bool checkMin=false], [bool checkMax=false])`](lua/convert3DCoordsToScreenEx.md) |
| [`float value = getStructFloatElement(uint struct, int offset, [bool unprotect=false])`](lua/getStructFloatElement.md) |
| [`setStructFloatElement(uint struct, int offset, float value, [bool unprotect=false])`](lua/setStructFloatElement.md) |
| [`bool state = wasKeyPressed(int key)`](lua/wasKeyPressed.md) |
| [`bool state = wasKeyReleased(int key)`](lua/wasKeyReleased.md) |
| [`int delta = getMousewheelDelta()`](lua/getMousewheelDelta.md) |
| [`consumeWindowMessage([bool game=true], [bool scripts=true])`](lua/consumeWindowMessage.md) |
| [`addEventHandler(string eventName, function callback)`](lua/addEventHandler.md) |
| [`bool paused = isGamePaused()`](lua/isGamePaused.md) |
| [`double time = gameClock()`](lua/gameClock.md) |
| [`script_properties(string property, ...)`](lua/script_properties.md) |
| [`script_url(string url)`](lua/script_url.md) |
| [`any imports = import(string filename)`](lua/import.md) |
| [`string json = encodeJson(table data)`](lua/encodeJson.md) |
| [`table data = decodeJson(string json)`](lua/decodeJson.md) |
| [`showCursor(bool show, [bool lockControls])`](lua/showCursor.md) |
| [`lockPlayerControl(bool lock)`](lua/lockPlayerControl.md) |
| [`bool locked = isPlayerControlLocked()`](lua/isPlayerControlLocked.md) |
| [`bool result = setBlipCoordinates(Marker blip, float x, float y, float z)`](lua/setBlipCoordinates.md) |
| [`bool result = setTargetBlipCoordinates(float x, float y, float z)`](lua/setTargetBlipCoordinates.md) |
| [`bool result = placeWaypoint(float x, float y, float z)`](lua/placeWaypoint.md) |
| [`bool result = removeWaypoint()`](lua/removeWaypoint.md) |
| [`string path = getFolderPath(int csidl)`](lua/getFolderPath.md) |
| [`float value = getTimeStepValue()`](lua/getTimeStepValue.md) |
| [`uint devicePtr = getD3DDevicePtr()`](lua/getD3DDevicePtr.md) |
| [`table objects = getAllObjects()`](lua/getAllObjects.md) |
| [`table peds = getAllChars()`](lua/getAllChars.md) |
| [`table vehicles = getAllVehicles()`](lua/getAllVehicles.md) |
| [`float value = getGameGlobalFloat(int index)`](lua/getGameGlobalFloat.md) |
| [`setGameGlobalFloat(int index, float value)`](lua/setGameGlobalFloat.md) |
| [`LuaScript s = script.load(string file)`](lua/script.load.md) |
| [`LuaScript s = script.find(string name)`](lua/script.find.md) |
| [`table list = script.list()`](lua/script.list.md) |
| [`LuaScript script = script.get(int scriptId)`](lua/script.get.md) |
| [`script.this`](lua/this.md) |
| [`table data = inicfg.load([table default], [string file])`](lua/inicfg.load.md) |
| [`bool result = inicfg.save(table data, [string file])`](lua/inicfg.save.md) |
| [`int value = memory.read(uint address, uint size, [bool unprotect=false])`](lua/memory.read.md) |
| [`memory.write(uint address, int value, uint size, [bool unprotect=false])`](lua/memory.write.md) |
| [`int value = memory.getint8(uint address, [bool unprotect=false])`](lua/memory.getint8.md) |
| [`bool result = memory.setint8(uint address, int byte, [bool unprotect=false])`](lua/memory.setint8.md) |
| [`int value = memory.getint16(uint address, [bool unprotect=false])`](lua/memory.getint16.md) |
| [`bool result = memory.setint16(uint address, int word, [bool unprotect=false])`](lua/memory.setint16.md) |
| [`int value = memory.getint32(uint address, [bool unprotect=false])`](lua/memory.getint32.md) |
| [`bool result = memory.setint32(uint address, int dword, [bool unprotect=false])`](lua/memory.setint32.md) |
| [`double value = memory.getint64(uint address, [bool unprotect=false])`](lua/memory.getint64.md) |
| [`bool result = memory.setint64(uint address, double qword, [bool unprotect=false])`](lua/memory.setint64.md) |
| [`int value = memory.getuint8(uint address, [bool unprotect=false])`](lua/memory.getuint8.md) |
| [`bool result = memory.setuint8(uint address, int byte, [bool unprotect=false])`](lua/memory.setuint8.md) |
| [`int value = memory.getuint16(uint address, [bool unprotect=false])`](lua/memory.getuint16.md) |
| [`bool result = memory.setuint16(uint address, int word, [bool unprotect=false])`](lua/memory.setuint16.md) |
| [`int value = memory.getuint32(uint address, [bool unprotect=false])`](lua/memory.getuint32.md) |
| [`bool result = memory.setuint32(uint address, int dword, [bool unprotect=false])`](lua/memory.setuint32.md) |
| [`double value = memory.getuint64(uint address, [bool unprotect=false])`](lua/memory.getuint64.md) |
| [`bool result = memory.setuint64(uint address, double qword, [bool unprotect=false])`](lua/memory.setuint64.md) |
| [`float value = memory.getfloat(uint address, [bool unprotect=false])`](lua/memory.getfloat.md) |
| [`bool result = memory.setfloat(uint address, float value, [bool unprotect=false])`](lua/memory.setfloat.md) |
| [`double value = memory.getdouble(uint address, [bool unprotect=false])`](lua/memory.getdouble.md) |
| [`bool result = memory.setdouble(uint address, double value, [bool unprotect=false])`](lua/memory.setdouble.md) |
| [`int oldProtection = memory.unprotect(uint address, uint size)`](lua/memory.unprotect.md) |
| [`int oldProtection = memory.protect(uint address, uint size, int newProtection)`](lua/memory.protect.md) |
| [`memory.copy(uint destAddress, uint srcAddress, uint size, [bool unprotect=false])`](lua/memory.copy.md) |
| [`bool result = memory.compare(uint address1, uint address2, uint size, [bool unprotect=false])`](lua/memory.compare.md) |
| [`string str = memory.tostring(uint address, [uint size], [bool unprotect=false])`](lua/memory.tostring.md) |
| [`string hexstr = memory.tohex(uint address, uint size, [bool unprotect=false])`](lua/memory.tohex.md) |
| [`bool result = memory.hex2bin(string hex, uint dstAddress, uint size)`](lua/memory.hex2bin.md) |
| [`string bin = memory.hex2bin(string hex)`](lua/memory.hex2bin.md) |
| [`memory.fill(uint address, int value, uint size, [bool unprotect=false])`](lua/memory.fill.md) |
| [`uint address = memory.strptr(string str)`](lua/memory.strptr.md) |
| [`LuaThread thread = lua_thread.create(function func, ...)`](lua/lua_thread.create.md) |
| [`LuaThread thread = lua_thread.create_suspended(function func)`](lua/lua_thread.create_suspended.md) |
| [`shakeCam(int shake)`](lua/shakeCam.md) |
| [`Player player = createPlayer(Model modelId, float atX, float atY, float atZ)`](lua/createPlayer.md) |
| [`Ped ped = createChar(int pedtype, Model modelId, float atX, float atY, float atZ)`](lua/createChar.md) |
| [`deleteChar(Ped ped)`](lua/deleteChar.md) |
| [`float positionX, float positionY, float positionZ = getCharCoordinates(Ped ped)`](lua/getCharCoordinates.md) |
| [`setCharCoordinates(Ped ped, float posX, float posY, float posZ)`](lua/setCharCoordinates.md) |
| [`bool result = isCharInArea2d(Ped ped, float cornerAX, float cornerAY, float cornerBX, float cornerBY, bool sphere)`](lua/isCharInArea2d.md) |
| [`bool result = isCharInArea3d(Ped ped, float cornerAX, float cornerAY, float cornerAZ, float cornerBX, float cornerBY, float cornerBZ, bool sphere)`](lua/isCharInArea3d.md) |
| [`Vehicle car = createCar(Model modelId, float atX, float atY, float atZ)`](lua/createCar.md) |
| [`deleteCar(Vehicle car)`](lua/deleteCar.md) |
| [`carGotoCoordinates(Vehicle car, float driveToX, float driveToY, float driveToZ)`](lua/carGotoCoordinates.md) |
| [`carWanderRandomly(Vehicle car)`](lua/carWanderRandomly.md) |
| [`carSetIdle(Vehicle car)`](lua/carSetIdle.md) |
| [`float positionX, float positionY, float positionZ = getCarCoordinates(Vehicle car)`](lua/getCarCoordinates.md) |
| [`setCarCoordinates(Vehicle car, float atX, float atY, float atZ)`](lua/setCarCoordinates.md) |
| [`setCarCruiseSpeed(Vehicle car, float maxSpeed)`](lua/setCarCruiseSpeed.md) |
| [`setCarDrivingStyle(Vehicle car, int behaviour)`](lua/setCarDrivingStyle.md) |
| [`setCarMission(Vehicle car, int driverBehaviour)`](lua/setCarMission.md) |
| [`bool result = isCarInArea2d(Vehicle car, float cornerAX, float cornerAY, float cornerBX, float cornerBY, bool sphere)`](lua/isCarInArea2d.md) |
| [`bool result = isCarInArea3d(Vehicle car, float cornerAX, float cornerAY, float cornerAZ, float cornerBX, float cornerBY, float cornerBZ, bool sphere)`](lua/isCarInArea3d.md) |
| [`printBig(GxtString gxtString, int time, int style)`](lua/printBig.md) |
| [`printText(GxtString gxtString, int time, int flag)`](lua/printText.md) |
| [`printTextNow(GxtString gxtString, int time, int flag)`](lua/printTextNow.md) |
| [`clearPrints()`](lua/clearPrints.md) |
| [`int hours, int mins = getTimeOfDay()`](lua/getTimeOfDay.md) |
| [`setTimeOfDay(int hours, int minutes)`](lua/setTimeOfDay.md) |
| [`int minutes = getMinutesToTimeOfDay(int hours, int minutes)`](lua/getMinutesToTimeOfDay.md) |
| [`bool result = isPointOnScreen(float sphereX, float sphereY, float sphereZ, float radius)`](lua/isPointOnScreen.md) |
| [`Vehicle car = storeCarCharIsIn(Ped ped)`](lua/storeCarCharIsIn.md) |
| [`bool result = isCharInCar(Ped ped, Vehicle car)`](lua/isCharInCar.md) |
| [`bool result = isCharInModel(Ped ped, Model carModel)`](lua/isCharInModel.md) |
| [`bool result = isCharInAnyCar(Ped ped)`](lua/isCharInAnyCar.md) |
| [`bool result = isButtonPressed(Player player, int key)`](lua/isButtonPressed.md) |
| [`int state = getPadState(Player player, int key)`](lua/getPadState.md) |
| [`bool result = locateCharAnyMeans2d(Ped ped, float pointX, float pointY, float radiusX, float radiusY, bool sphere)`](lua/locateCharAnyMeans2d.md) |
| [`bool result = locateCharOnFoot2d(Ped ped, float pointX, float pointY, float radiusX, float radiusY, bool sphere)`](lua/locateCharOnFoot2d.md) |
| [`bool result = locateCharInCar2d(Ped ped, float pointX, float pointY, float radiusX, float radiusY, bool sphere)`](lua/locateCharInCar2d.md) |
| [`bool result = locateStoppedCharAnyMeans2d(Ped ped, float pointX, float pointY, float radiusX, float radiusY, bool sphere)`](lua/locateStoppedCharAnyMeans2d.md) |
| [`bool result = locateStoppedCharOnFoot2d(Ped ped, float pointX, float pointY, float radiusX, float radiusY, bool sphere)`](lua/locateStoppedCharOnFoot2d.md) |
| [`bool result = locateStoppedCharInCar2d(Ped ped, float pointX, float pointY, float radiusX, float radiusY, bool sphere)`](lua/locateStoppedCharInCar2d.md) |
| [`bool result = locateCharAnyMeansChar2d(Ped ped, Ped nearPed, float radiusX, float radiusY, bool sphere)`](lua/locateCharAnyMeansChar2d.md) |
| [`locateCharOnFootChar2d(Ped ped, Ped nearPed, float radiusX, float radiusY, bool sphere)`](lua/locateCharOnFootChar2d.md) |
| [`bool result = locateCharInCarChar2d(Ped ped, Ped nearPed, float radiusX, float radiusY, bool sphere)`](lua/locateCharInCarChar2d.md) |
| [`bool result = locateCharAnyMeans3d(Ped ped, float sphereX, float sphereY, float sphereZ, float radiusX, float radiusY, float radiusZ, bool sphere)`](lua/locateCharAnyMeans3d.md) |
| [`bool result = locateCharOnFoot3d(Ped ped, float sphereX, float sphereY, float sphereZ, float radiusX, float radiusY, float radiusZ, bool sphere)`](lua/locateCharOnFoot3d.md) |
| [`bool result = locateCharInCar3d(Ped ped, float sphereX, float sphereY, float sphereZ, float radiusX, float radiusY, float radiusZ, bool sphere)`](lua/locateCharInCar3d.md) |
| [`bool result = locateStoppedCharAnyMeans3d(Ped ped, float sphereX, float sphereY, float sphereZ, float radiusX, float radiusY, float radiusZ, bool sphere)`](lua/locateStoppedCharAnyMeans3d.md) |
| [`bool result = locateStoppedCharOnFoot3d(Ped ped, float sphereX, float sphereY, float sphereZ, float radiusX, float radiusY, float radiusZ, bool sphere)`](lua/locateStoppedCharOnFoot3d.md) |
| [`bool result = locateStoppedCharInCar3d(Ped ped, float sphereX, float sphereY, float sphereZ, float radiusX, float radiusY, float radiusZ, bool sphere)`](lua/locateStoppedCharInCar3d.md) |
| [`bool result = locateCharAnyMeansChar3d(Ped ped, Ped nearPed, float radiusX, float radiusY, float radiusZ, bool sphere)`](lua/locateCharAnyMeansChar3d.md) |
| [`bool result = locateCharOnFootChar3d(Ped ped, Ped nearPed, float radiusX, float radiusY, float radiusZ, bool sphere)`](lua/locateCharOnFootChar3d.md) |
| [`bool result = locateCharInCarChar3d(Ped ped, Ped nearPed, float radiusX, float radiusY, float radiusZ, bool sphere)`](lua/locateCharInCarChar3d.md) |
| [`Object object = createObject(Model modelId, float atX, float atY, float atZ)`](lua/createObject.md) |
| [`deleteObject(Object object)`](lua/deleteObject.md) |
| [`givePlayerMoney(Player player, int money)`](lua/givePlayerMoney.md) |
| [`int money = getPlayerMoney(Player player)`](lua/getPlayerMoney.md) |
| [`giveRemoteControlledCarToPlayer(Player player, float float2, float float3, float float4)`](lua/giveRemoteControlledCarToPlayer.md) |
| [`alterWantedLevel(Player player, int wantedLevel)`](lua/alterWantedLevel.md) |
| [`alterWantedLevelNoDrop(Player player, int minimumWantedLevel)`](lua/alterWantedLevelNoDrop.md) |
| [`bool result = isWantedLevelGreater(Player player, int level)`](lua/isWantedLevelGreater.md) |
| [`clearWantedLevel(Player player)`](lua/clearWantedLevel.md) |
| [`setDeatharrestState(bool value)`](lua/setDeatharrestState.md) |
| [`bool result = hasDeatharrestBeenExecuted()`](lua/hasDeatharrestBeenExecuted.md) |
| [`addAmmoToChar(Ped ped, int weapon, int ammo)`](lua/addAmmoToChar.md) |
| [`bool result = isPlayerDead(Player player)`](lua/isPlayerDead.md) |
| [`bool result = isCharDead(Ped ped)`](lua/isCharDead.md) |
| [`bool result = isCarDead(Vehicle car)`](lua/isCarDead.md) |
| [`bool result = isPlayerPressingHorn(Player player)`](lua/isPlayerPressingHorn.md) |
| [`Ped ped = createCharInsideCar(Vehicle car, Model pedtype, int model)`](lua/createCharInsideCar.md) |
| [`bool result = isCarModel(Vehicle car, Model modelId)`](lua/isCarModel.md) |
| [`int carGenerator = createCarGenerator(float atX, float atY, float atZ, float angle, Model modelId, int color1, int color2, bool forceSpawn, int alarm, int doorLock, int minDelay, int maxDelay)`](lua/createCarGenerator.md) |
| [`switchCarGenerator(int carGenerator, int carsToGenerate)`](lua/switchCarGenerator.md) |
| [`displayOnscreenTimer(VarId var, bool countInDirection)`](lua/displayOnscreenTimer.md) |
| [`clearOnscreenTimer(VarId var)`](lua/clearOnscreenTimer.md) |
| [`clearOnscreenCounter(VarId var)`](lua/clearOnscreenCounter.md) |
| [`bool result = isCharInZone(Ped ped, GxtString zoneName)`](lua/isCharInZone.md) |
| [`pointCameraAtCar(Vehicle car, int mode, int switchstyle)`](lua/pointCameraAtCar.md) |
| [`pointCameraAtChar(Ped ped, int mode, int switchstyle)`](lua/pointCameraAtChar.md) |
| [`restoreCamera()`](lua/restoreCamera.md) |
| [`shakePad(Player player, int time, int intensity)`](lua/shakePad.md) |
| [`setTimeScale(float gamespeed)`](lua/setTimeScale.md) |
| [`setFixedCameraPosition(float positionX, float positionY, float positionZ, float rotationX, float rotationY, float rotationZ)`](lua/setFixedCameraPosition.md) |
| [`pointCameraAtPoint(float pointAtX, float pointAtY, float pointAtZ, int switchstyle)`](lua/pointCameraAtPoint.md) |
| [`Marker marker = addBlipForCarOld(Vehicle car, int unused, bool visibility)`](lua/addBlipForCarOld.md) |
| [`Marker marker = addBlipForCharOld(Ped ped, int int2, int int3)`](lua/addBlipForCharOld.md) |
| [`removeBlip(Marker marker)`](lua/removeBlip.md) |
| [`changeBlipColour(Marker marker, int color)`](lua/changeBlipColour.md) |
| [`Marker marker = addBlipForCoordOld(float atX, float atY, float atZ, int color, int flag)`](lua/addBlipForCoordOld.md) |
| [`changeBlipScale(Marker marker, int size)`](lua/changeBlipScale.md) |
| [`setFadingColour(int r, int g, int b)`](lua/setFadingColour.md) |
| [`doFade(bool in, int time)`](lua/doFade.md) |
| [`bool result = getFadingStatus()`](lua/getFadingStatus.md) |
| [`addHospitalRestart(float atX, float atY, float atZ, float angle, int townNumber)`](lua/addHospitalRestart.md) |
| [`addPoliceRestart(float atX, float atY, float atZ, float angle, int townNumber)`](lua/addPoliceRestart.md) |
| [`overrideNextRestart(float atX, float atY, float atZ, float angle)`](lua/overrideNextRestart.md) |
| [`drawShadow(Particle particle, float atX, float atY, float atZ, float rotationFactor, float size, int intensity, int flags1, int flags2, int flags3)`](lua/drawShadow.md) |
| [`float angle = getCharHeading(Ped ped)`](lua/getCharHeading.md) |
| [`setCharHeading(Ped ped, float angle)`](lua/setCharHeading.md) |
| [`float angle = getCarHeading(Vehicle car)`](lua/getCarHeading.md) |
| [`setCarHeading(Vehicle car, float angle)`](lua/setCarHeading.md) |
| [`float angle = getObjectHeading(Object object)`](lua/getObjectHeading.md) |
| [`setObjectHeading(Object object, float angle)`](lua/setObjectHeading.md) |
| [`bool result = isCharTouchingObject(Ped ped, Object object)`](lua/isCharTouchingObject.md) |
| [`setCharAmmo(Ped ped, int weapon, int ammo)`](lua/setCharAmmo.md) |
| [`declareMissionFlag(VarId flag)`](lua/declareMissionFlag.md) |
| [`Marker marker = addBlipForCar(Vehicle car)`](lua/addBlipForCar.md) |
| [`Marker marker = addBlipForChar(Ped ped)`](lua/addBlipForChar.md) |
| [`Marker marker = addBlipForObject(Object object)`](lua/addBlipForObject.md) |
| [`Checkpoint checkpoint = addBlipForCoord(float atX, float atY, float atZ)`](lua/addBlipForCoord.md) |
| [`changeBlipDisplay(Marker marker, int mode)`](lua/changeBlipDisplay.md) |
| [`addOneOffSound(float atX, float atY, float atZ, int sound)`](lua/addOneOffSound.md) |
| [`int unk = addContinuousSound(float atX, float atY, float atZ, int sound)`](lua/addContinuousSound.md) |
| [`removeSound(int sound)`](lua/removeSound.md) |
| [`bool result = isCarStuckOnRoof(Vehicle car)`](lua/isCarStuckOnRoof.md) |
| [`addUpsidedownCarCheck(Vehicle car)`](lua/addUpsidedownCarCheck.md) |
| [`removeUpsidedownCarCheck(Vehicle car)`](lua/removeUpsidedownCarCheck.md) |
| [`bool result = isCharInAreaOnFoot2d(Ped ped, float cornerAX, float cornerAY, float cornerBX, float cornerBY, bool sphere)`](lua/isCharInAreaOnFoot2d.md) |
| [`bool result = isCharInAreaInCar2d(Ped ped, float cornerAX, float cornerAY, float cornerBX, float cornerBY, bool sphere)`](lua/isCharInAreaInCar2d.md) |
| [`bool result = isCharStoppedInArea2d(Ped ped, float cornerAX, float cornerAY, float cornerBX, float cornerBY, bool sphere)`](lua/isCharStoppedInArea2d.md) |
| [`bool result = isCharStoppedInAreaOnFoot2d(Ped ped, float cornerAX, float cornerAY, float cornerBX, float cornerBY, bool sphere)`](lua/isCharStoppedInAreaOnFoot2d.md) |
| [`bool result = isCharStoppedInAreaInCar2d(Ped ped, float cornerAX, float cornerAY, float cornerBX, float cornerBY, bool sphere)`](lua/isCharStoppedInAreaInCar2d.md) |
| [`bool result = isCharInAreaOnFoot3d(Ped ped, float cornerAX, float cornerAY, float cornerAZ, float cornerBX, float cornerBY, float cornerBZ, bool sphere)`](lua/isCharInAreaOnFoot3d.md) |
| [`bool result = isCharInAreaInCar3d(Ped ped, float cornerAX, float cornerAY, float cornerAZ, float cornerBX, float cornerBY, float cornerBZ, bool sphere)`](lua/isCharInAreaInCar3d.md) |
| [`bool result = isCharStoppedInArea3d(Ped ped, float cornerAX, float cornerAY, float cornerAZ, float cornerBX, float cornerBY, float cornerBZ, bool sphere)`](lua/isCharStoppedInArea3d.md) |
| [`bool result = isCharStoppedInAreaOnFoot3d(Ped ped, float cornerAX, float cornerAY, float cornerAZ, float cornerBX, float cornerBY, float cornerBZ, bool sphere)`](lua/isCharStoppedInAreaOnFoot3d.md) |
| [`bool result = isCharStoppedInAreaInCar3d(Ped ped, float cornerAX, float cornerAY, float cornerAZ, float cornerBX, float cornerBY, float cornerBZ, bool sphere)`](lua/isCharStoppedInAreaInCar3d.md) |
| [`bool result = isCarStoppedInArea2d(Vehicle car, float cornerAX, float cornerAY, float cornerBX, float cornerBY, bool sphere)`](lua/isCarStoppedInArea2d.md) |
| [`bool result = isCarStoppedInArea3d(Vehicle car, float cornerAX, float cornerAY, float cornerAZ, float cornerBX, float cornerBY, float cornerBZ, bool sphere)`](lua/isCarStoppedInArea3d.md) |
| [`bool result = locateCar2d(Vehicle car, float pointX, float pointY, float radiusX, float radiusY, bool sphere)`](lua/locateCar2d.md) |
| [`bool result = locateStoppedCar2d(Vehicle car, float pointX, float pointY, float radiusX, float radiusY, bool sphere)`](lua/locateStoppedCar2d.md) |
| [`bool result = locateCar3d(Vehicle car, float sphereX, float sphereY, float sphereZ, float radiusX, float radiusY, float radiusZ, bool sphere)`](lua/locateCar3d.md) |
| [`bool result = locateStoppedCar3d(Vehicle car, float sphereX, float sphereY, float sphereZ, float radiusX, float radiusY, float radiusZ, bool sphere)`](lua/locateStoppedCar3d.md) |
| [`giveWeaponToChar(Ped ped, int weapon, int ammo)`](lua/giveWeaponToChar.md) |
| [`bool result = setPlayerControl(Player player, bool canMove)`](lua/setPlayerControl.md) |
| [`bool result = forceWeather(int weather)`](lua/forceWeather.md) |
| [`bool result = forceWeatherNow(int weather)`](lua/forceWeatherNow.md) |
| [`releaseWeather()`](lua/releaseWeather.md) |
| [`setCurrentCharWeapon(Ped ped, int weapon)`](lua/setCurrentCharWeapon.md) |
| [`bool result, float positionX, float positionY, float positionZ = getObjectCoordinates(Object object)`](lua/getObjectCoordinates.md) |
| [`bool result = setObjectCoordinates(Object object, float atX, float atY, float atZ)`](lua/setObjectCoordinates.md) |
| [`int timeMs = getGameTimer()`](lua/getGameTimer.md) |
| [`bool result, int level = storeWantedLevel(Player player)`](lua/storeWantedLevel.md) |
| [`bool result = isCarStopped(Vehicle car)`](lua/isCarStopped.md) |
| [`markCharAsNoLongerNeeded(Ped ped)`](lua/markCharAsNoLongerNeeded.md) |
| [`markCarAsNoLongerNeeded(Vehicle car)`](lua/markCarAsNoLongerNeeded.md) |
| [`markObjectAsNoLongerNeeded(Object object)`](lua/markObjectAsNoLongerNeeded.md) |
| [`dontRemoveChar(Ped ped)`](lua/dontRemoveChar.md) |
| [`dontRemoveObject(Object object)`](lua/dontRemoveObject.md) |
| [`bool result, Ped ped = createCharAsPassenger(Vehicle car, Model pedtype, int model, int passengerSeat)`](lua/createCharAsPassenger.md) |
| [`bool result = printWithNumberBig(GxtString gxtString, int number, int time, int style)`](lua/printWithNumberBig.md) |
| [`bool result = printWithNumber(GxtString gxtString, int number, int time, int flag)`](lua/printWithNumber.md) |
| [`bool result = printWithNumberNow(GxtString gxtString, int number, int time, int flag)`](lua/printWithNumberNow.md) |
| [`bool result = switchRoadsOn(float cornerAX, float cornerAY, float cornerAZ, float cornerBX, float cornerBY, float cornerBZ)`](lua/switchRoadsOn.md) |
| [`switchRoadsOff(float cornerAX, float cornerAY, float cornerAZ, float cornerBX, float cornerBY, float cornerBZ)`](lua/switchRoadsOff.md) |
| [`bool result, int passengers = getNumberOfPassengers(Vehicle car)`](lua/getNumberOfPassengers.md) |
| [`int maxPassengers = getMaximumNumberOfPassengers(Vehicle car)`](lua/getMaximumNumberOfPassengers.md) |
| [`bool result = setCarDensityMultiplier(float multiplier)`](lua/setCarDensityMultiplier.md) |
| [`bool result = setCarHeavy(Vehicle car, bool heavy)`](lua/setCarHeavy.md) |
| [`setMaxWantedLevel(int level)`](lua/setMaxWantedLevel.md) |
| [`bool result = isCarInAirProper(Vehicle car)`](lua/isCarInAirProper.md) |
| [`bool result = isCarUpsidedown(Vehicle car)`](lua/isCarUpsidedown.md) |
| [`bool result, Ped ped = getPlayerChar(Player player)`](lua/getPlayerChar.md) |
| [`bool result = cancelOverrideRestart()`](lua/cancelOverrideRestart.md) |
| [`bool result = setPoliceIgnorePlayer(Player player, bool ignored)`](lua/setPoliceIgnorePlayer.md) |
| [`bool result = startKillFrenzy(GxtString gxtString, int weapon, int timeLimit, int targets, Model targetModels1, Model targetModels2, Model targetModels3, Model targetModels4, bool completedText)`](lua/startKillFrenzy.md) |
| [`bool result, int status = readKillFrenzyStatus()`](lua/readKillFrenzyStatus.md) |
| [`bool result = locateCharAnyMeansCar2d(Ped ped, Vehicle car, float radiusX, float radiusY, bool sphere)`](lua/locateCharAnyMeansCar2d.md) |
| [`bool result = locateCharOnFootCar2d(Ped ped, Vehicle car, float radiusX, float radiusY, bool flag)`](lua/locateCharOnFootCar2d.md) |
| [`bool result = locateCharInCarCar2d(Ped ped, Vehicle car, float radiusX, float radiusY, bool sphere)`](lua/locateCharInCarCar2d.md) |
| [`bool result = locateCharAnyMeansCar3d(Ped ped, Vehicle car, float radiusX, float radiusY, float radiusZ, bool flag)`](lua/locateCharAnyMeansCar3d.md) |
| [`bool result = locateCharOnFootCar3d(Ped ped, Vehicle car, float radiusX, float radiusY, float radiusZ, bool flag)`](lua/locateCharOnFootCar3d.md) |
| [`bool result = locateCharInCarCar3d(Ped ped, Vehicle car, float radiusX, float radiusY, float radiusZ, bool flag)`](lua/locateCharInCarCar3d.md) |
| [`lockCarDoors(Vehicle car, int status)`](lua/lockCarDoors.md) |
| [`bool result = explodeCar(Vehicle car)`](lua/explodeCar.md) |
| [`bool result = addExplosion(float atX, float atY, float atZ, int radius)`](lua/addExplosion.md) |
| [`bool result = isCarUpright(Vehicle car)`](lua/isCarUpright.md) |
| [`bool result, Pickup pickup = createPickup(Model modelId, int type, float atX, float atY, float atZ)`](lua/createPickup.md) |
| [`bool result = hasPickupBeenCollected(Pickup pickup)`](lua/hasPickupBeenCollected.md) |
| [`bool result = removePickup(Pickup pickup)`](lua/removePickup.md) |
| [`bool result = setTaxiLights(Vehicle taxi, bool light)`](lua/setTaxiLights.md) |
| [`bool result = printBigQ(GxtString gxtString, int time, int style)`](lua/printBigQ.md) |
| [`bool result = setTargetCarForMissionGarage(GxtString garage, Vehicle car)`](lua/setTargetCarForMissionGarage.md) |
| [`bool result = applyBrakesToPlayersCar(Player player, bool apply)`](lua/applyBrakesToPlayersCar.md) |
| [`setCharHealth(Ped ped, int health)`](lua/setCharHealth.md) |
| [`setCarHealth(Vehicle car, int health)`](lua/setCarHealth.md) |
| [`int health = getCharHealth(Ped ped)`](lua/getCharHealth.md) |
| [`int health = getCarHealth(Vehicle car)`](lua/getCarHealth.md) |
| [`bool result = changeCarColour(Vehicle car, int primaryColor, int secondaryColor)`](lua/changeCarColour.md) |
| [`switchPedRoadsOn(float cornerAX, float cornerAY, float cornerAZ, float cornerBX, float cornerBY, float cornerBZ)`](lua/switchPedRoadsOn.md) |
| [`switchPedRoadsOff(float cornerAX, float cornerAY, float cornerAZ, float cornerBX, float cornerBY, float cornerBZ)`](lua/switchPedRoadsOff.md) |
| [`setGangWeapons(int gang, int weapons1, int weapons2, int weapons3)`](lua/setGangWeapons.md) |
| [`bool result = isCharTouchingObjectOnFoot(Ped ped, Object object)`](lua/isCharTouchingObjectOnFoot.md) |
| [`loadSpecialCharacter(GxtString gxtString, int id)`](lua/loadSpecialCharacter.md) |
| [`bool result = hasSpecialCharacterLoaded(int id)`](lua/hasSpecialCharacterLoaded.md) |
| [`bool result = isPlayerInRemoteMode(Player player)`](lua/isPlayerInRemoteMode.md) |
| [`setCutsceneOffset(float posX, float posY, float posZ)`](lua/setCutsceneOffset.md) |
| [`setAnimGroupForChar(Ped ped, string style)`](lua/setAnimGroupForChar.md) |
| [`requestModel(Model modelId)`](lua/requestModel.md) |
| [`bool result = hasModelLoaded(Model modelId)`](lua/hasModelLoaded.md) |
| [`markModelAsNoLongerNeeded(Model modelId)`](lua/markModelAsNoLongerNeeded.md) |
| [`drawCorona(float atX, float atY, float atZ, float radius, int type, bool lensflares, int r, int g, int b)`](lua/drawCorona.md) |
| [`storeClock()`](lua/storeClock.md) |
| [`restoreClock()`](lua/restoreClock.md) |
| [`bool result = isPlayerPlaying(Player player)`](lua/isPlayerPlaying.md) |
| [`int mode = getControllerMode()`](lua/getControllerMode.md) |
| [`setCanResprayCar(Vehicle car, bool sprayable)`](lua/setCanResprayCar.md) |
| [`unloadSpecialCharacter(int id)`](lua/unloadSpecialCharacter.md) |
| [`resetNumOfModelsKilledByPlayer(Player player)`](lua/resetNumOfModelsKilledByPlayer.md) |
| [`int quantity = getNumOfModelsKilledByPlayer(Player player, Model modelId)`](lua/getNumOfModelsKilledByPlayer.md) |
| [`activateGarage(GxtString garage)`](lua/activateGarage.md) |
| [`Object object = createObjectNoOffset(Model modelId, float atX, float atY, float atZ)`](lua/createObjectNoOffset.md) |
| [`bool result = isCharStopped(Ped ped)`](lua/isCharStopped.md) |
| [`switchWidescreen(bool enable)`](lua/switchWidescreen.md) |
| [`Marker marker = addSpriteBlipForContactPoint(float atX, float atY, float atZ, int icon)`](lua/addSpriteBlipForContactPoint.md) |
| [`Marker marker = addSpriteBlipForCoord(float atX, float atY, float atZ, int type)`](lua/addSpriteBlipForCoord.md) |
| [`setCharOnlyDamagedByPlayer(Ped ped, bool enabled)`](lua/setCharOnlyDamagedByPlayer.md) |
| [`setCarOnlyDamagedByPlayer(Vehicle car, bool enabled)`](lua/setCarOnlyDamagedByPlayer.md) |
| [`setCharProofs(Ped ped, bool BP, bool FP, bool EP, bool CP, bool MP)`](lua/setCharProofs.md) |
| [`setCarProofs(Vehicle car, bool BP, bool FP, bool EP, bool CP, bool MP)`](lua/setCarProofs.md) |
| [`deactivateGarage(GxtString garage)`](lua/deactivateGarage.md) |
| [`bool result = isCarInWater(Vehicle car)`](lua/isCarInWater.md) |
| [`float nodeX, float nodeY, float nodeZ = getClosestCharNode(float closestToX, float closestToY, float closestToZ)`](lua/getClosestCharNode.md) |
| [`float nodeX, float nodeY, float nodeZ = getClosestCarNode(float closestToX, float closestToY, float closestToZ)`](lua/getClosestCarNode.md) |
| [`carGotoCoordinatesAccurate(Vehicle car, float toX, float toY, float toZ)`](lua/carGotoCoordinatesAccurate.md) |
| [`bool result = isCarOnScreen(Vehicle car)`](lua/isCarOnScreen.md) |
| [`bool result = isCharOnScreen(Ped ped)`](lua/isCharOnScreen.md) |
| [`bool result = isObjectOnScreen(Object object)`](lua/isObjectOnScreen.md) |
| [`float z = getGroundZFor3dCoord(float atX, float atY, float atZ)`](lua/getGroundZFor3dCoord.md) |
| [`int fire = startScriptFire(float atX, float atY, float atZ, int propagation, int size)`](lua/startScriptFire.md) |
| [`bool result = isScriptFireExtinguished(int fire)`](lua/isScriptFireExtinguished.md) |
| [`removeScriptFire(int fire)`](lua/removeScriptFire.md) |
| [`boatGotoCoords(Vehicle boat, float toX, float toY, float toZ)`](lua/boatGotoCoords.md) |
| [`boatStop(Vehicle car)`](lua/boatStop.md) |
| [`bool result = isCharShootingInArea(Ped ped, float cornerAX, float cornerAY, float cornerBX, float cornerBY, int weapon)`](lua/isCharShootingInArea.md) |
| [`bool result = isCurrentCharWeapon(Ped ped, int weapon)`](lua/isCurrentCharWeapon.md) |
| [`setBoatCruiseSpeed(Vehicle boat, float speed)`](lua/setBoatCruiseSpeed.md) |
| [`Ped ped = getRandomCharInZone(GxtString zone, bool pedtype, bool gang, bool criminal_prostitute)`](lua/getRandomCharInZone.md) |
| [`bool result = isCharShooting(Ped ped)`](lua/isCharShooting.md) |
| [`Pickup pickup = createMoneyPickup(float atX, float atY, float atZ, int cash, bool permanenceFlag)`](lua/createMoneyPickup.md) |
| [`setCharAccuracy(Ped ped, int accuracy)`](lua/setCharAccuracy.md) |
| [`float speed = getCarSpeed(Vehicle car)`](lua/getCarSpeed.md) |
| [`loadCutscene(GxtString cutscene)`](lua/loadCutscene.md) |
| [`Object object = createCutsceneObject(Model modelId)`](lua/createCutsceneObject.md) |
| [`setCutsceneAnim(int cutscene, GxtString anim)`](lua/setCutsceneAnim.md) |
| [`startCutscene()`](lua/startCutscene.md) |
| [`int time = getCutsceneTime()`](lua/getCutsceneTime.md) |
| [`bool result = hasCutsceneFinished()`](lua/hasCutsceneFinished.md) |
| [`clearCutscene()`](lua/clearCutscene.md) |
| [`restoreCameraJumpcut()`](lua/restoreCameraJumpcut.md) |
| [`setCollectable1Total(int total)`](lua/setCollectable1Total.md) |
| [`bool result = isProjectileInArea(float cornerAX, float cornerAY, float cornerAZ, float cornerBX, float cornerBY, float cornerBZ)`](lua/isProjectileInArea.md) |
| [`bool result = isCharModel(Ped ped, Model modelId)`](lua/isCharModel.md) |
| [`loadSpecialModel(Model modelId, GxtString gxtString)`](lua/loadSpecialModel.md) |
| [`float forwardX = getCarForwardX(Vehicle car)`](lua/getCarForwardX.md) |
| [`float forwardY = getCarForwardY(Vehicle car)`](lua/getCarForwardY.md) |
| [`changeGarageType(GxtString garage, int type)`](lua/changeGarageType.md) |
| [`printWith2NumbersNow(GxtString gxtString, int numbers1, int numbers2, int time, int flag)`](lua/printWith2NumbersNow.md) |
| [`printWith3Numbers(GxtString gxtString, int numbers1, int numbers2, int numbers3, int time, int flag)`](lua/printWith3Numbers.md) |
| [`printWith4Numbers(GxtString gxtString, int numbers1, int numbers2, int numbers3, int numbers4, int time, int flag)`](lua/printWith4Numbers.md) |
| [`printWith4NumbersNow(GxtString gxtString, int numbers1, int numbers2, int numbers3, int numbers4, int time, int flag)`](lua/printWith4NumbersNow.md) |
| [`printWith6Numbers(GxtString gxtString, int numbers1, int numbers2, int numbers3, int numbers4, int numbers5, int numbers6, int time, int flag)`](lua/printWith6Numbers.md) |
| [`playerMadeProgress(int progress)`](lua/playerMadeProgress.md) |
| [`setProgressTotal(int maxProgress)`](lua/setProgressTotal.md) |
| [`registerMissionGiven()`](lua/registerMissionGiven.md) |
| [`registerMissionPassed(GxtString mission)`](lua/registerMissionPassed.md) |
| [`removeAllScriptFires()`](lua/removeAllScriptFires.md) |
| [`bool result = hasCharBeenDamagedByWeapon(Ped ped, int weapon)`](lua/hasCharBeenDamagedByWeapon.md) |
| [`bool result = hasCarBeenDamagedByWeapon(Vehicle car, int weapon)`](lua/hasCarBeenDamagedByWeapon.md) |
| [`explodeCharHead(Ped ped)`](lua/explodeCharHead.md) |
| [`anchorBoat(Vehicle boat, bool anchor)`](lua/anchorBoat.md) |
| [`int fire = startCarFire(Vehicle car)`](lua/startCarFire.md) |
| [`int fire = startCharFire(Ped ped)`](lua/startCharFire.md) |
| [`Vehicle car = getRandomCarOfTypeInArea(float cornerAX, float cornerAY, float cornerBX, float cornerBY, Model modelId)`](lua/getRandomCarOfTypeInArea.md) |
| [`bool result = hasResprayHappened(Vehicle car)`](lua/hasResprayHappened.md) |
| [`setCameraZoom(int mode)`](lua/setCameraZoom.md) |
| [`Pickup pickup = createPickupWithAmmo(Model modelId, int type, int ammo, float atX, float atY, float atZ)`](lua/createPickupWithAmmo.md) |
| [`setCarRamCar(Vehicle car, Vehicle car)`](lua/setCarRamCar.md) |
| [`setPlayerNeverGetsTired(Player player, bool infiniteRun)`](lua/setPlayerNeverGetsTired.md) |
| [`setPlayerFastReload(Player player, bool fastReload)`](lua/setPlayerFastReload.md) |
| [`setCharBleeding(Ped ped, bool bleeding)`](lua/setCharBleeding.md) |
| [`setFreeResprays(bool enable)`](lua/setFreeResprays.md) |
| [`setCharVisible(Ped ped, bool visible)`](lua/setCharVisible.md) |
| [`setCarVisible(Vehicle car, bool visible)`](lua/setCarVisible.md) |
| [`bool result = isAreaOccupied(float cornerAX, float cornerAY, float cornerAZ, float cornerBX, float cornerBY, float cornerBZ, bool solid, bool car, bool actor, bool object, bool particle)`](lua/isAreaOccupied.md) |
| [`displayText(float posX, float posY, GxtString gxtString)`](lua/displayText.md) |
| [`setTextScale(float sizeX, float sizeY)`](lua/setTextScale.md) |
| [`setTextColour(int r, int g, int b, int a)`](lua/setTextColour.md) |
| [`setTextJustify(bool alignJustify)`](lua/setTextJustify.md) |
| [`setTextCentre(bool centered)`](lua/setTextCentre.md) |
| [`setTextWrapx(float linewidth)`](lua/setTextWrapx.md) |
| [`setTextCentreSize(float linewidth)`](lua/setTextCentreSize.md) |
| [`setTextBackground(bool background)`](lua/setTextBackground.md) |
| [`setTextProportional(bool proportional)`](lua/setTextProportional.md) |
| [`setTextFont(int font)`](lua/setTextFont.md) |
| [`bool result = rotateObject(Object object, float fromAngle, float toAngle, bool flag)`](lua/rotateObject.md) |
| [`bool result = slideObject(Object object, float toX, float toY, float toZ, float speedX, float speedY, float speedZ, bool collisionCheck)`](lua/slideObject.md) |
| [`removeCharElegantly(Ped ped)`](lua/removeCharElegantly.md) |
| [`setCharStayInSamePlace(Ped ped, bool enabled)`](lua/setCharStayInSamePlace.md) |
| [`bool result = isExplosionInArea(int explosionType, float cornerAX, float cornerAY, float cornerAZ, float cornerBX, float cornerBY, float cornerBZ)`](lua/isExplosionInArea.md) |
| [`placeObjectRelativeToCar(Object object, Vehicle car, float offsetX, float offsetY, float offsetZ)`](lua/placeObjectRelativeToCar.md) |
| [`makeObjectTargettable(Object object, bool targetable)`](lua/makeObjectTargettable.md) |
| [`addArmourToChar(Ped ped, int points)`](lua/addArmourToChar.md) |
| [`openGarage(GxtString garage)`](lua/openGarage.md) |
| [`closeGarage(GxtString garage)`](lua/closeGarage.md) |
| [`warpCharFromCarToCoord(Ped ped, float placeAtX, float placeAtY, float placeAtZ)`](lua/warpCharFromCarToCoord.md) |
| [`setVisibilityOfClosestObjectOfType(float atX, float atY, float atZ, float radius, Model modelId, bool visibility)`](lua/setVisibilityOfClosestObjectOfType.md) |
| [`bool result = hasCharSpottedChar(Ped ped, Ped ped)`](lua/hasCharSpottedChar.md) |
| [`bool result = hasObjectBeenDamaged(Object object)`](lua/hasObjectBeenDamaged.md) |
| [`warpCharIntoCar(Ped ped, Vehicle car)`](lua/warpCharIntoCar.md) |
| [`printWith2NumbersBig(GxtString gxtString, int numbers1, int numbers2, int time, int style)`](lua/printWith2NumbersBig.md) |
| [`setCameraBehindPlayer()`](lua/setCameraBehindPlayer.md) |
| [`Ped ped = createRandomChar(float atX, float atY, float atZ)`](lua/createRandomChar.md) |
| [`bool result = isSniperBulletInArea(float float1, float float2, float float3, float float4, float float5, float float6)`](lua/isSniperBulletInArea.md) |
| [`setObjectVelocity(Object object, float velocityInDirectionX, float velocityInDirectionY, float velocityInDirectionZ)`](lua/setObjectVelocity.md) |
| [`setObjectCollision(Object object, bool collision)`](lua/setObjectCollision.md) |
| [`printStringInStringNow(GxtString gxtString, GxtString string, int time1, int time2)`](lua/printStringInStringNow.md) |
| [`bool result = isPointObscuredByAMissionEntity(float cornerAX, float cornerAY, float cornerAZ, float cornerBX, float cornerBY, float cornerBZ)`](lua/isPointObscuredByAMissionEntity.md) |
| [`loadAllModelsNow()`](lua/loadAllModelsNow.md) |
| [`addToObjectVelocity(Object object, float velocityX, float velocityY, float velocityZ)`](lua/addToObjectVelocity.md) |
| [`drawSprite(int texture, float positionX, float positionY, float width, float height, int r, int g, int b, int a)`](lua/drawSprite.md) |
| [`drawRect(float positionX, float positionY, float width, float height, int r, int g, int b, int a)`](lua/drawRect.md) |
| [`int id = loadSprite(string name)`](lua/loadSprite.md) |
| [`bool result = loadTextureDictionary(zstring txd)`](lua/loadTextureDictionary.md) |
| [`removeTextureDictionary()`](lua/removeTextureDictionary.md) |
| [`setObjectDynamic(Object object, bool moveable)`](lua/setObjectDynamic.md) |
| [`setCharAnimSpeed(Ped ped, string animation, float speed)`](lua/setCharAnimSpeed.md) |
| [`playMissionPassedTune(int music)`](lua/playMissionPassedTune.md) |
| [`clearArea(float atX, float atY, float atZ, float radius, bool area)`](lua/clearArea.md) |
| [`freezeOnscreenTimer(bool timer)`](lua/freezeOnscreenTimer.md) |
| [`switchCarSiren(Vehicle car, bool siren)`](lua/switchCarSiren.md) |
| [`setCarWatertight(Vehicle car, bool watertight)`](lua/setCarWatertight.md) |
| [`setCharCantBeDraggedOut(Ped ped, bool locked)`](lua/setCharCantBeDraggedOut.md) |
| [`turnCarToFaceCoord(Vehicle car, float coordX, float coordY)`](lua/turnCarToFaceCoord.md) |
| [`drawSphere(float atX, float atY, float atZ, float radius)`](lua/drawSphere.md) |
| [`setCarStatus(Vehicle car, int action)`](lua/setCarStatus.md) |
| [`bool result = isCharMale(Ped ped)`](lua/isCharMale.md) |
| [`policeRadioMessage(float float1, float float2, float float3)`](lua/policeRadioMessage.md) |
| [`setCarStrong(Vehicle car, bool strong)`](lua/setCarStrong.md) |
| [`switchRubbish(bool int1)`](lua/switchRubbish.md) |
| [`switchStreaming(bool streaming)`](lua/switchStreaming.md) |
| [`bool result = isGarageOpen(GxtString garage)`](lua/isGarageOpen.md) |
| [`bool result = isGarageClosed(GxtString garage)`](lua/isGarageClosed.md) |
| [`swapNearestBuildingModel(float atX, float atY, float atZ, float radius, Model from, Model to)`](lua/swapNearestBuildingModel.md) |
| [`switchWorldProcessing(bool cutsceneOnly)`](lua/switchWorldProcessing.md) |
| [`clearAreaOfCars(float cornerAX, float cornerAY, float cornerAZ, float cornerBX, float cornerBY, float cornerBZ)`](lua/clearAreaOfCars.md) |
| [`int sphere = addSphere(float atX, float atY, float atZ, float radius)`](lua/addSphere.md) |
| [`removeSphere(int sphere)`](lua/removeSphere.md) |
| [`setEveryoneIgnorePlayer(Player player, bool ignored)`](lua/setEveryoneIgnorePlayer.md) |
| [`Vehicle car = storeCarCharIsInNoSave(Ped ped)`](lua/storeCarCharIsInNoSave.md) |
| [`displayOnscreenTimerWithString(VarId timer, int type, GxtString gxtString)`](lua/displayOnscreenTimerWithString.md) |
| [`displayOnscreenCounterWithString(VarId var, bool type, GxtString gxtString)`](lua/displayOnscreenCounterWithString.md) |
| [`createRandomCarForCarPark(float coordsX, float coordsY, float coordsZ, float zAngle)`](lua/createRandomCarForCarPark.md) |
| [`setWantedMultiplier(float sensitivity)`](lua/setWantedMultiplier.md) |
| [`setCameraInFrontOfPlayer()`](lua/setCameraInFrontOfPlayer.md) |
| [`bool result = isCarVisiblyDamaged(Vehicle car)`](lua/isCarVisiblyDamaged.md) |
| [`bool result = doesObjectExist(Object object)`](lua/doesObjectExist.md) |
| [`loadScene(float atX, float atY, float atZ)`](lua/loadScene.md) |
| [`addStuckCarCheck(Vehicle car, float stuckCheckDistance, int time)`](lua/addStuckCarCheck.md) |
| [`removeStuckCarCheck(Vehicle car)`](lua/removeStuckCarCheck.md) |
| [`bool result = isCarStuck(Vehicle car)`](lua/isCarStuck.md) |
| [`loadMissionAudio(int asId, int name)`](lua/loadMissionAudio.md) |
| [`bool result = hasMissionAudioLoaded(int id)`](lua/hasMissionAudioLoaded.md) |
| [`playMissionAudio(int id)`](lua/playMissionAudio.md) |
| [`bool result = hasMissionAudioFinished(int id)`](lua/hasMissionAudioFinished.md) |
| [`float nodeX, float nodeY, float nodeZ, float angle = getClosestCarNodeWithHeading(float X, float Y, float Z)`](lua/getClosestCarNodeWithHeading.md) |
| [`bool result = hasImportGarageSlotBeenFilled(int int1, int int2)`](lua/hasImportGarageSlotBeenFilled.md) |
| [`clearThisPrint(GxtString text)`](lua/clearThisPrint.md) |
| [`clearThisBigPrint(GxtString text)`](lua/clearThisBigPrint.md) |
| [`setMissionAudioPosition(int id, float locationX, float locationY, float locationZ)`](lua/setMissionAudioPosition.md) |
| [`activateSaveMenu()`](lua/activateSaveMenu.md) |
| [`bool result = hasSaveGameFinished()`](lua/hasSaveGameFinished.md) |
| [`noSpecialCameraForThisGarage(int int1)`](lua/noSpecialCameraForThisGarage.md) |
| [`Marker marker = addBlipForPickup(Pickup pickup)`](lua/addBlipForPickup.md) |
| [`setPedDensityMultiplier(float multiplier)`](lua/setPedDensityMultiplier.md) |
| [`setTextDrawBeforeFade(bool int1)`](lua/setTextDrawBeforeFade.md) |
| [`int collected = getCollectable1sCollected()`](lua/getCollectable1sCollected.md) |
| [`setSpritesDrawBeforeFade(bool antialiased)`](lua/setSpritesDrawBeforeFade.md) |
| [`setTextRightJustify(bool alignRight)`](lua/setTextRightJustify.md) |
| [`printHelp(GxtString gxtString)`](lua/printHelp.md) |
| [`clearHelp()`](lua/clearHelp.md) |
| [`flashHudObject(int hudComponent)`](lua/flashHudObject.md) |
| [`setGenerateCarsAroundCamera(bool int1)`](lua/setGenerateCarsAroundCamera.md) |
| [`clearSmallPrints()`](lua/clearSmallPrints.md) |
| [`setUpsidedownCarNotDamaged(Vehicle car, bool disableFlippedExplosion)`](lua/setUpsidedownCarNotDamaged.md) |
| [`bool result = isPlayerControllable(Player player)`](lua/isPlayerControllable.md) |
| [`makePlayerSafe(Player player)`](lua/makePlayerSafe.md) |
| [`int primaryColor, int secondaryColor = getCarColours(Vehicle car)`](lua/getCarColours.md) |
| [`setAllCarsCanBeDamaged(bool enable)`](lua/setAllCarsCanBeDamaged.md) |
| [`setCarCanBeDamaged(Vehicle car, bool enable)`](lua/setCarCanBeDamaged.md) |
| [`setDrunkInputDelay(Player player, int handlingResponsiveness)`](lua/setDrunkInputDelay.md) |
| [`setCharMoney(Ped ped, int money)`](lua/setCharMoney.md) |
| [`float X, float Y, float Z = getOffsetFromObjectInWorldCoords(Object object, float offsetX, float offsetY, float offsetZ)`](lua/getOffsetFromObjectInWorldCoords.md) |
| [`float X, float Y, float Z = getOffsetFromCarInWorldCoords(Vehicle car, float offsetX, float offsetY, float offsetZ)`](lua/getOffsetFromCarInWorldCoords.md) |
| [`clearMissionAudio(int id)`](lua/clearMissionAudio.md) |
| [`setFreeHealthCare(Player player, bool free)`](lua/setFreeHealthCare.md) |
| [`loadAndLaunchMissionInternal(int mission)`](lua/loadAndLaunchMissionInternal.md) |
| [`setObjectDrawLast(Object object, bool drawLast)`](lua/setObjectDrawLast.md) |
| [`int ammo = getAmmoInCharWeapon(Ped ped, int int)`](lua/getAmmoInCharWeapon.md) |
| [`setNearClip(float clip)`](lua/setNearClip.md) |
| [`setRadioChannel(int radioStation)`](lua/setRadioChannel.md) |
| [`setCarTraction(Vehicle car, float traction)`](lua/setCarTraction.md) |
| [`bool result = areMeasurementsInMetres()`](lua/areMeasurementsInMetres.md) |
| [`float feet = convertMetresToFeet(float meters)`](lua/convertMetresToFeet.md) |
| [`setCarAvoidLevelTransitions(Vehicle car, bool avoidLevelTransitions)`](lua/setCarAvoidLevelTransitions.md) |
| [`clearAreaOfChars(float cornerAX, float cornerAY, float cornerAZ, float cornerBX, float cornerBY, float cornerBZ)`](lua/clearAreaOfChars.md) |
| [`setTotalNumberOfMissions(int totalMissions)`](lua/setTotalNumberOfMissions.md) |
| [`int imperial = convertMetresToFeetInt(int metric)`](lua/convertMetresToFeetInt.md) |
| [`registerFastestTime(int stat, int to)`](lua/registerFastestTime.md) |
| [`registerHighestScore(int int1, int int2)`](lua/registerHighestScore.md) |
| [`warpCharIntoCarAsPassenger(Ped ped, Vehicle car, int passengerSeat)`](lua/warpCharIntoCarAsPassenger.md) |
| [`bool result = isCarPassengerSeatFree(Vehicle car, int seat)`](lua/isCarPassengerSeatFree.md) |
| [`Ped ped = getCharInCarPassengerSeat(Vehicle car, int seat)`](lua/getCharInCarPassengerSeat.md) |
| [`setCharIsChrisCriminal(Ped ped, bool flag)`](lua/setCharIsChrisCriminal.md) |
| [`startCredits()`](lua/startCredits.md) |
| [`stopCredits()`](lua/stopCredits.md) |
| [`bool result = areCreditsFinished()`](lua/areCreditsFinished.md) |
| [`setMusicDoesFade(bool enable)`](lua/setMusicDoesFade.md) |
| [`Model modelId = getCarModel(Vehicle veh)`](lua/getCarModel.md) |
| [`bool result = areAnyCarCheatsActivated()`](lua/areAnyCarCheatsActivated.md) |
| [`setCharSuffersCriticalHits(Ped ped, bool enable)`](lua/setCharSuffersCriticalHits.md) |
| [`bool result = isCharSittingInCar(Ped ped, Vehicle car)`](lua/isCharSittingInCar.md) |
| [`bool result = isCharSittingInAnyCar(Ped ped)`](lua/isCharSittingInAnyCar.md) |
| [`bool result = isCharOnFoot(Ped ped)`](lua/isCharOnFoot.md) |
| [`loadSplashScreen(GxtString gxtString)`](lua/loadSplashScreen.md) |
| [`setJamesCarOnPathToPlayer(int int1)`](lua/setJamesCarOnPathToPlayer.md) |
| [`setObjectRotation(Object object, float rotationX, float rotationY, float rotationZ)`](lua/setObjectRotation.md) |
| [`float X, float Y, float Z = getDebugCameraCoordinates()`](lua/getDebugCameraCoordinates.md) |
| [`bool result = isPlayerTargettingChar(Player player, Ped ped)`](lua/isPlayerTargettingChar.md) |
| [`bool result = isPlayerTargettingObject(Player player, Object object)`](lua/isPlayerTargettingObject.md) |
| [`displayTextWithNumber(float x, float y, GxtString gxtString, int number)`](lua/displayTextWithNumber.md) |
| [`displayTextWith2Numbers(float x, float y, GxtString gxtString, int numbersX, int numbersY)`](lua/displayTextWith2Numbers.md) |
| [`failCurrentMission()`](lua/failCurrentMission.md) |
| [`setInterpolationParameters(float delay, int time)`](lua/setInterpolationParameters.md) |
| [`float X, float Y, float Z = getDebugCameraPointAt()`](lua/getDebugCameraPointAt.md) |
| [`attachCharToCar(Ped ped, Vehicle car, float offsetX, float offsetY, float offsetZ, int position, float shootingAngleLimit, int weapon)`](lua/attachCharToCar.md) |
| [`detachCharFromCar(Ped ped)`](lua/detachCharFromCar.md) |
| [`setCarStayInFastLane(Vehicle car, bool flag)`](lua/setCarStayInFastLane.md) |
| [`clearCharLastWeaponDamage(Ped ped)`](lua/clearCharLastWeaponDamage.md) |
| [`clearCarLastWeaponDamage(Vehicle car)`](lua/clearCarLastWeaponDamage.md) |
| [`int int10 = getRandomCopInArea(float float1, float float2, float float3, float float4, bool int5, bool int6, bool int7, bool int8, bool int9)`](lua/getRandomCopInArea.md) |
| [`Ped ped = getDriverOfCar(Vehicle car)`](lua/getDriverOfCar.md) |
| [`int followers = getNumberOfFollowers(Ped ped)`](lua/getNumberOfFollowers.md) |
| [`giveRemoteControlledModelToPlayer(Player player, float atX, float atY, float atZ, float angle, Model RCModel)`](lua/giveRemoteControlledModelToPlayer.md) |
| [`int weapon = getCurrentCharWeapon(Ped ped)`](lua/getCurrentCharWeapon.md) |
| [`bool result = locateCharAnyMeansObject2d(Ped ped, Object object, float radiusX, float radiusY, bool sphere)`](lua/locateCharAnyMeansObject2d.md) |
| [`bool result = locateCharOnFootObject2d(Ped ped, Object object, float radiusX, float radiusY, bool sphere)`](lua/locateCharOnFootObject2d.md) |
| [`bool result = locateCharInCarObject2d(Ped ped, Object object, float radiusX, float radiusY, bool sphere)`](lua/locateCharInCarObject2d.md) |
| [`bool result = locateCharAnyMeansObject3d(Ped ped, Object object, float radiusX, float radiusY, float radiusZ, bool sphere)`](lua/locateCharAnyMeansObject3d.md) |
| [`bool result = locateCharOnFootObject3d(Ped ped, Object object, float radiusX, float radiusY, float radiusZ, bool sphere)`](lua/locateCharOnFootObject3d.md) |
| [`bool result = locateCharInCarObject3d(Ped ped, Object object, float radiusX, float radiusY, float radiusZ, bool sphere)`](lua/locateCharInCarObject3d.md) |
| [`setCarTempAction(Vehicle car, int action, int time)`](lua/setCarTempAction.md) |
| [`bool result = isCharOnAnyBike(Ped ped)`](lua/isCharOnAnyBike.md) |
| [`bool result = canCharSeeDeadChar(Ped ped, int pedtype)`](lua/canCharSeeDeadChar.md) |
| [`setEnterCarRangeMultiplier(float float1)`](lua/setEnterCarRangeMultiplier.md) |
| [`Vehicle car = getRemoteControlledCar(Player player)`](lua/getRemoteControlledCar.md) |
| [`bool result = isPcVersion()`](lua/isPcVersion.md) |
| [`bool result = isModelAvailable(Model modelId)`](lua/isModelAvailable.md) |
| [`shutCharUp(Ped ped, bool muted)`](lua/shutCharUp.md) |
| [`setEnableRcDetonate(bool detonation)`](lua/setEnableRcDetonate.md) |
| [`setCarRandomRouteSeed(Vehicle car, int routeSeed)`](lua/setCarRandomRouteSeed.md) |
| [`bool result = isAnyPickupAtCoords(float pickupX, float pickupY, float pickupZ)`](lua/isAnyPickupAtCoords.md) |
| [`removeAllCharWeapons(Ped ped)`](lua/removeAllCharWeapons.md) |
| [`bool result = hasCharGotWeapon(Ped ped, int weapon)`](lua/hasCharGotWeapon.md) |
| [`setTankDetonateCars(int tank, bool detonate)`](lua/setTankDetonateCars.md) |
| [`int offset1, int offset2, int offset3, int offset4 = getPositionOfAnalogueSticks(int joystick)`](lua/getPositionOfAnalogueSticks.md) |
| [`bool result = isCarOnFire(Vehicle car)`](lua/isCarOnFire.md) |
| [`bool result = isCarTireBurst(Vehicle car, int tire)`](lua/isCarTireBurst.md) |
| [`initialiseObjectPath(int int1, float float2)`](lua/initialiseObjectPath.md) |
| [`setObjectPathSpeed(int int1, int int2)`](lua/setObjectPathSpeed.md) |
| [`setObjectPathPosition(int int1, float float2)`](lua/setObjectPathPosition.md) |
| [`clearObjectPath(int int1)`](lua/clearObjectPath.md) |
| [`heliGotoCoords(Vehicle heli, float toX, float toY, float toZ, float altitudeMin, float altitudeMax)`](lua/heliGotoCoords.md) |
| [`float coordsX, float coordsY, float coordsZ = getDeadCharPickupCoords(Ped ped)`](lua/getDeadCharPickupCoords.md) |
| [`Pickup pickup = createProtectionPickup(float atX, float atY, float atZ, int int4, int int5)`](lua/createProtectionPickup.md) |
| [`bool result = isCharInAnyBoat(Ped ped)`](lua/isCharInAnyBoat.md) |
| [`bool result = isCharInAnyHeli(Ped ped)`](lua/isCharInAnyHeli.md) |
| [`bool result = isCharInAnyPlane(Ped ped)`](lua/isCharInAnyPlane.md) |
| [`bool result = isCharInWater(Ped ped)`](lua/isCharInWater.md) |
| [`int weapon, int ammo, Model modelId = getCharWeaponInSlot(Ped ped, int slot)`](lua/getCharWeaponInSlot.md) |
| [`float float6, float float7, float float8, float float9, float float10, float float11, float float12 = getClosestStraightRoad(float atX, float atY, float atZ, float height, float radius)`](lua/getClosestStraightRoad.md) |
| [`setCarForwardSpeed(Vehicle car, float speed)`](lua/setCarForwardSpeed.md) |
| [`setInteriorVisible(int interior)`](lua/setInteriorVisible.md) |
| [`markCarAsConvoyCar(Vehicle car, bool convoy)`](lua/markCarAsConvoyCar.md) |
| [`resetHavocCausedByPlayer(int int1)`](lua/resetHavocCausedByPlayer.md) |
| [`int int2 = getHavocCausedByPlayer(int int1)`](lua/getHavocCausedByPlayer.md) |
| [`createScriptRoadblock(float cornerAX, float cornerAY, float cornerAZ, float cornerBX, float cornerBY, float cornerBZ, int type)`](lua/createScriptRoadblock.md) |
| [`clearAllScriptRoadblocks()`](lua/clearAllScriptRoadblocks.md) |
| [`float X, float Y, float Z = getOffsetFromCharInWorldCoords(Ped ped, float offsetX, float offsetY, float offsetZ)`](lua/getOffsetFromCharInWorldCoords.md) |
| [`bool result = hasCharBeenPhotographed(Ped ped)`](lua/hasCharBeenPhotographed.md) |
| [`switchSecurityCamera(bool int1)`](lua/switchSecurityCamera.md) |
| [`bool result = isCharInFlyingVehicle(Ped ped)`](lua/isCharInFlyingVehicle.md) |
| [`Marker marker = addShortRangeSpriteBlipForCoord(float atX, float atY, float atZ, int icon)`](lua/addShortRangeSpriteBlipForCoord.md) |
| [`setHeliOrientation(Vehicle heli, float angle)`](lua/setHeliOrientation.md) |
| [`clearHeliOrientation(Vehicle heli)`](lua/clearHeliOrientation.md) |
| [`planeGotoCoords(int plane, float X, float Y, float Z, float z1, float z2)`](lua/planeGotoCoords.md) |
| [`float X, float Y, float Z = getNthClosestCarNode(float X, float Y, float Z, int type)`](lua/getNthClosestCarNode.md) |
| [`drawWeaponshopCorona(float X, float Y, float Z, float radius, int type, int flare, int r, int g, int b)`](lua/drawWeaponshopCorona.md) |
| [`setEnableRcDetonateOnContact(bool enable)`](lua/setEnableRcDetonateOnContact.md) |
| [`freezeCharPosition(Ped ped, bool locked)`](lua/freezeCharPosition.md) |
| [`setCharDrownsInWater(Ped ped, bool drowns)`](lua/setCharDrownsInWater.md) |
| [`setObjectRecordsCollisions(Object object, bool set)`](lua/setObjectRecordsCollisions.md) |
| [`bool result = hasObjectCollidedWithAnything(Object object)`](lua/hasObjectCollidedWithAnything.md) |
| [`removeRcBuggy()`](lua/removeRcBuggy.md) |
| [`int armour = getCharArmour(Ped ped)`](lua/getCharArmour.md) |
| [`setHeliStabiliser(Vehicle heli, bool limiter)`](lua/setHeliStabiliser.md) |
| [`setCarStraightLineDistance(Vehicle car, int radius)`](lua/setCarStraightLineDistance.md) |
| [`popCarBoot(Vehicle car)`](lua/popCarBoot.md) |
| [`shutPlayerUp(Player player, bool shut)`](lua/shutPlayerUp.md) |
| [`setPlayerMood(Player player, int flag, int time)`](lua/setPlayerMood.md) |
| [`requestCollision(float X, float Y)`](lua/requestCollision.md) |
| [`bool result = locateObject2d(Object object, float X, float Y, float radiusX, float radiusY, bool sphere)`](lua/locateObject2d.md) |
| [`bool result = locateObject3d(Object object, float X, float Y, float Z, float radiusX, float radiusY, float radiusZ, bool flag)`](lua/locateObject3d.md) |
| [`bool result = isObjectInWater(Object object)`](lua/isObjectInWater.md) |
| [`bool result = isObjectInArea2d(Object object, float cornerAX, float cornerAY, float cornerBX, float cornerBY, bool sphere)`](lua/isObjectInArea2d.md) |
| [`bool result = isObjectInArea3d(Object object, float cornerAX, float cornerAY, float cornerAZ, float cornerBX, float cornerBY, float cornerBZ, bool flag)`](lua/isObjectInArea3d.md) |
| [`taskToggleDuck(Ped ped, bool crouch)`](lua/taskToggleDuck.md) |
| [`requestAnimation(string animation)`](lua/requestAnimation.md) |
| [`bool result = hasAnimationLoaded(string animation)`](lua/hasAnimationLoaded.md) |
| [`removeAnimation(string animation)`](lua/removeAnimation.md) |
| [`bool result = isCharWaitingForWorldCollision(Ped ped)`](lua/isCharWaitingForWorldCollision.md) |
| [`bool result = isCarWaitingForWorldCollision(Vehicle car)`](lua/isCarWaitingForWorldCollision.md) |
| [`attachCharToObject(Ped ped, Object object, float offsetX, float offsetY, float offsetZ, int orientation, float angle, int lockWeapon)`](lua/attachCharToObject.md) |
| [`displayNthOnscreenCounterWithString(VarId text, int type, int line, GxtString gxtString)`](lua/displayNthOnscreenCounterWithString.md) |
| [`addSetPiece(int type, float rectX1, float rectY1, float rectX2, float rectY2, float spawnAX, float spawnAY, float headedTowards1X, float headedTowards1Y, float spawnBX, float spawnBY, float headedTowards2X, float headedTowards2Y)`](lua/addSetPiece.md) |
| [`setExtraColours(int color, bool fade)`](lua/setExtraColours.md) |
| [`clearExtraColours(bool fade)`](lua/clearExtraColours.md) |
| [`int twowheelstime, float twowheelsdistance, int wheelietime, float wheelieDistance, int stoppieTime, float stoppieDistance = getWheelieStats(Player player)`](lua/getWheelieStats.md) |
| [`burstCarTire(Vehicle car, int tire)`](lua/burstCarTire.md) |
| [`bool result = isPlayerWearing(Player player, string bodypart, int skin)`](lua/isPlayerWearing.md) |
| [`setPlayerCanDoDriveBy(Player player, bool mode)`](lua/setPlayerCanDoDriveBy.md) |
| [`int handleAs = createSwatRope(int pedtype, Model modelId, float X, float Y, float Z)`](lua/createSwatRope.md) |
| [`setCarModelComponents(Model car, int variation1, int variation2)`](lua/setCarModelComponents.md) |
| [`closeAllCarDoors(Vehicle car)`](lua/closeAllCarDoors.md) |
| [`float distance = getDistanceBetweenCoords2d(float x1, float y1, float x2, float y2)`](lua/getDistanceBetweenCoords2d.md) |
| [`float distance = getDistanceBetweenCoords3d(float x1, float y1, float z1, float x2, float y2, float z2)`](lua/getDistanceBetweenCoords3d.md) |
| [`sortOutObjectCollisionWithCar(Object object, Vehicle car)`](lua/sortOutObjectCollisionWithCar.md) |
| [`int level = getMaxWantedLevel()`](lua/getMaxWantedLevel.md) |
| [`printHelpForever(GxtString text)`](lua/printHelpForever.md) |
| [`printHelpForeverWithNumber(GxtString text, int number)`](lua/printHelpForeverWithNumber.md) |
| [`Pickup pickup = createLockedPropertyPickup(float pX, float pY, float pZ, GxtString gxtString)`](lua/createLockedPropertyPickup.md) |
| [`Pickup pickup = createForsalePropertyPickup(float pX, float pY, float pZ, int price, GxtString gxtString)`](lua/createForsalePropertyPickup.md) |
| [`freezeCarPosition(Vehicle car, bool locked)`](lua/freezeCarPosition.md) |
| [`bool result = hasCharBeenDamagedByChar(Ped ped, Ped byActor)`](lua/hasCharBeenDamagedByChar.md) |
| [`bool result = hasCharBeenDamagedByCar(Ped ped, Vehicle byCar)`](lua/hasCharBeenDamagedByCar.md) |
| [`bool result = hasCarBeenDamagedByChar(Vehicle car, Ped byActor)`](lua/hasCarBeenDamagedByChar.md) |
| [`bool result = hasCarBeenDamagedByCar(Vehicle car, Vehicle byCar)`](lua/hasCarBeenDamagedByCar.md) |
| [`int radio = getRadioChannel()`](lua/getRadioChannel.md) |
| [`setCharStayInCarWhenJacked(Ped ped, bool stay)`](lua/setCharStayInCarWhenJacked.md) |
| [`setPlayerDrunkenness(Player player, int drunk)`](lua/setPlayerDrunkenness.md) |
| [`Vehicle car = getRandomCarOfTypeInAreaNoSave(float x1, float y1, float x2, float y2, Model modelId)`](lua/getRandomCarOfTypeInAreaNoSave.md) |
| [`setCanBurstCarTires(Vehicle car, bool vulnerability)`](lua/setCanBurstCarTires.md) |
| [`fireHunterGun(Vehicle car)`](lua/fireHunterGun.md) |
| [`bool result = isCharTouchingVehicle(Ped ped, Vehicle car)`](lua/isCharTouchingVehicle.md) |
| [`setCharCanBeShotInVehicle(Ped ped, bool can)`](lua/setCharCanBeShotInVehicle.md) |
| [`loadMissionText(GxtString table)`](lua/loadMissionText.md) |
| [`clearCharLastDamageEntity(Ped ped)`](lua/clearCharLastDamageEntity.md) |
| [`clearCarLastDamageEntity(Vehicle car)`](lua/clearCarLastDamageEntity.md) |
| [`freezeObjectPosition(Object object, bool freeze)`](lua/freezeObjectPosition.md) |
| [`removeWeaponFromChar(Ped ped, int weapon)`](lua/removeWeaponFromChar.md) |
| [`makePlayerFireProof(Player player, bool fireproof)`](lua/makePlayerFireProof.md) |
| [`increasePlayerMaxHealth(Player player, int increase)`](lua/increasePlayerMaxHealth.md) |
| [`increasePlayerMaxArmour(Player player, int increase)`](lua/increasePlayerMaxArmour.md) |
| [`Ped ped = createRandomCharAsDriver(Vehicle car)`](lua/createRandomCharAsDriver.md) |
| [`Ped ped = createRandomCharAsPassenger(Vehicle car, int seat)`](lua/createRandomCharAsPassenger.md) |
| [`ensurePlayerHasDriveByWeapon(Player player, int ammo)`](lua/ensurePlayerHasDriveByWeapon.md) |
| [`makeHeliComeCrashingDown(Vehicle heli)`](lua/makeHeliComeCrashingDown.md) |
| [`addExplosionNoSound(float pX, float pY, float pZ, int type)`](lua/addExplosionNoSound.md) |
| [`linkObjectToInterior(Object object, int interior)`](lua/linkObjectToInterior.md) |
| [`setCharNeverTargetted(Ped ped, bool untargetable)`](lua/setCharNeverTargetted.md) |
| [`bool result = wasCutsceneSkipped()`](lua/wasCutsceneSkipped.md) |
| [`bool result = isCharInAnyPoliceVehicle(Ped ped)`](lua/isCharInAnyPoliceVehicle.md) |
| [`bool result = doesCharExist(Ped ped)`](lua/doesCharExist.md) |
| [`bool result = doesVehicleExist(Vehicle car)`](lua/doesVehicleExist.md) |
| [`Marker blip = addShortRangeSpriteBlipForContactPoint(float pX, float pY, float pZ, int icon)`](lua/addShortRangeSpriteBlipForContactPoint.md) |
| [`setAllTaxisHaveNitro(bool toggle)`](lua/setAllTaxisHaveNitro.md) |
| [`freezeCarPositionAndDontLoadCollision(Vehicle car, bool keep)`](lua/freezeCarPositionAndDontLoadCollision.md) |
| [`freezeCharPositionAndDontLoadCollision(Ped ped, bool keep)`](lua/freezeCharPositionAndDontLoadCollision.md) |
| [`setPlayerIsInStadium(bool set)`](lua/setPlayerIsInStadium.md) |
| [`displayRadar(bool enable)`](lua/displayRadar.md) |
| [`registerBestPosition(int stat, float float)`](lua/registerBestPosition.md) |
| [`bool result = isPlayerInInfoZone(Player player, GxtString zone)`](lua/isPlayerInInfoZone.md) |
| [`setLoadCollisionForCarFlag(Vehicle car, bool enable)`](lua/setLoadCollisionForCarFlag.md) |
| [`setLoadCollisionForCharFlag(Ped ped, bool enable)`](lua/setLoadCollisionForCharFlag.md) |
| [`addBigGunFlash(float fromX, float fromY, float fromZ, float toX, float toY, float toZ)`](lua/addBigGunFlash.md) |
| [`float progress = getProgressPercentage()`](lua/getProgressPercentage.md) |
| [`setVehicleToFadeIn(Vehicle car, int flag)`](lua/setVehicleToFadeIn.md) |
| [`registerOddjobMissionPassed()`](lua/registerOddjobMissionPassed.md) |
| [`bool result = isPlayerInShortcutTaxi(Player player)`](lua/isPlayerInShortcutTaxi.md) |
| [`bool result = isCharDucking(Ped ped)`](lua/isCharDucking.md) |
| [`setOnscreenCounterFlashWhenFirstDisplayed(VarId text, bool flashing)`](lua/setOnscreenCounterFlashWhenFirstDisplayed.md) |
| [`shuffleCardDecks(bool shuffle)`](lua/shuffleCardDecks.md) |
| [`int card = fetchNextCard()`](lua/fetchNextCard.md) |
| [`float vecX, float vecY, float vecZ = getObjectVelocity(Object object)`](lua/getObjectVelocity.md) |
| [`bool result = isDebugCameraOn()`](lua/isDebugCameraOn.md) |
| [`addToObjectRotationVelocity(Object object, float vecX, float vecY, float vecZ)`](lua/addToObjectRotationVelocity.md) |
| [`setObjectRotationVelocity(Object object, float vecX, float vecY, float vecZ)`](lua/setObjectRotationVelocity.md) |
| [`bool result = isObjectStatic(Object object)`](lua/isObjectStatic.md) |
| [`float angle = getAngleBetween2dVectors(float vecX, float vecY, float vecX, float vecY)`](lua/getAngleBetween2dVectors.md) |
| [`bool result = do2dRectanglesCollide(float areaX, float areaY, float scaleX, float scaleY, float overlapareaX, float overlapareaY, float overlapscaleX, float overlapscaleY)`](lua/do2dRectanglesCollide.md) |
| [`float axisX, float axisY, float axisZ = getObjectRotationVelocity(Object object)`](lua/getObjectRotationVelocity.md) |
| [`addVelocityRelativeToObjectVelocity(Object object, float vecX, float vecY, float vecZ)`](lua/addVelocityRelativeToObjectVelocity.md) |
| [`float speed = getObjectSpeed(Object object)`](lua/getObjectSpeed.md) |
| [`bool result, float X, float Y = get2dLinesIntersectPoint(float l1x1, float l1y1, float l1x2, float l1y2, float l2x1, float l2y1, float l2x2, float l2y2)`](lua/get2dLinesIntersectPoint.md) |
| [`taskPause(Ped ped, int timeMS)`](lua/taskPause.md) |
| [`taskStandStill(Ped ped, int timeMS)`](lua/taskStandStill.md) |
| [`taskFallAndGetUp(Ped ped, bool int2, int time)`](lua/taskFallAndGetUp.md) |
| [`taskJump(Ped ped, bool jump)`](lua/taskJump.md) |
| [`taskTired(Ped ped, int timeMS)`](lua/taskTired.md) |
| [`taskDie(Ped ped)`](lua/taskDie.md) |
| [`taskLookAtChar(Ped ped, int lookAt, int timeMS)`](lua/taskLookAtChar.md) |
| [`taskLookAtVehicle(Ped ped, int lookAt, int timeMS)`](lua/taskLookAtVehicle.md) |
| [`taskSay(Ped ped, int audio)`](lua/taskSay.md) |
| [`taskShakeFist(Ped ped)`](lua/taskShakeFist.md) |
| [`taskCower(Ped ped)`](lua/taskCower.md) |
| [`taskHandsUp(Ped ped, int timeMS)`](lua/taskHandsUp.md) |
| [`taskDuck(Ped ped, int timeMS)`](lua/taskDuck.md) |
| [`taskUseAtm(Ped ped)`](lua/taskUseAtm.md) |
| [`taskScratchHead(Ped ped)`](lua/taskScratchHead.md) |
| [`taskLookAbout(Ped ped, int timeMS)`](lua/taskLookAbout.md) |
| [`taskEnterCarAsPassenger(Ped ped, Vehicle car, int time, int passengerSeat)`](lua/taskEnterCarAsPassenger.md) |
| [`taskEnterCarAsDriver(Ped ped, Vehicle car, int timeMS)`](lua/taskEnterCarAsDriver.md) |
| [`taskLeaveCar(Ped ped, Vehicle car)`](lua/taskLeaveCar.md) |
| [`taskLeaveCarAndFlee(Ped ped, Vehicle car, float X, float Y, float Z)`](lua/taskLeaveCarAndFlee.md) |
| [`taskCarDriveToCoord(Ped ped, Vehicle car, float toX, float toY, float toZ, float speed, int int7, int model, int int9)`](lua/taskCarDriveToCoord.md) |
| [`taskCarDriveWander(Ped ped, Vehicle hijackCar, float searchRadius, int trafficBehavior)`](lua/taskCarDriveWander.md) |
| [`taskGoStraightToCoord(Ped ped, float toX, float toY, float toZ, int mode, int time)`](lua/taskGoStraightToCoord.md) |
| [`taskAchieveHeading(Ped ped, float angle)`](lua/taskAchieveHeading.md) |
| [`flushRoute()`](lua/flushRoute.md) |
| [`extendRoute(float pointX, float pointY, float pointZ)`](lua/extendRoute.md) |
| [`taskFollowPointRoute(Ped ped, int flags1, int flags2)`](lua/taskFollowPointRoute.md) |
| [`taskGotoChar(Ped ped, Ped toActor, int timelimit, float stopWithinRadius)`](lua/taskGotoChar.md) |
| [`taskFleePoint(Ped ped, float fromX, float fromY, float fromZ, float awayRadius, int timelimit)`](lua/taskFleePoint.md) |
| [`taskFleeChar(Ped ped, Ped fromActor, float radius, int timelimit)`](lua/taskFleeChar.md) |
| [`taskSmartFleePoint(Ped ped, float fromX, float fromY, float fromZ, float stopAtRadius, int timelimit)`](lua/taskSmartFleePoint.md) |
| [`taskSmartFleeChar(Ped ped, Ped fromActor, float originRadius, int timelimit)`](lua/taskSmartFleeChar.md) |
| [`taskWanderStandard(Ped ped)`](lua/taskWanderStandard.md) |
| [`taskKillCharOnFoot(Ped ped, Ped killActor)`](lua/taskKillCharOnFoot.md) |
| [`startPlaybackRecordedCar(Vehicle car, int path)`](lua/startPlaybackRecordedCar.md) |
| [`stopPlaybackRecordedCar(Vehicle car)`](lua/stopPlaybackRecordedCar.md) |
| [`pausePlaybackRecordedCar(Vehicle car)`](lua/pausePlaybackRecordedCar.md) |
| [`unpausePlaybackRecordedCar(Vehicle car)`](lua/unpausePlaybackRecordedCar.md) |
| [`setCarEscortCarLeft(Vehicle car, Vehicle followCar)`](lua/setCarEscortCarLeft.md) |
| [`setCarEscortCarRight(Vehicle car, Vehicle followCar)`](lua/setCarEscortCarRight.md) |
| [`setCarEscortCarRear(Vehicle car, Vehicle followCar)`](lua/setCarEscortCarRear.md) |
| [`setCarEscortCarFront(Vehicle car, Vehicle followCar)`](lua/setCarEscortCarFront.md) |
| [`taskFollowPathNodesToCoord(Ped ped, float pathX, float pathY, float pathZ, int mode, int time)`](lua/taskFollowPathNodesToCoord.md) |
| [`bool result = isCharInAngledArea2d(Ped ped, float x1, float y1, float x2, float y2, float angle, bool sphere)`](lua/isCharInAngledArea2d.md) |
| [`bool result = isCharInAngledAreaOnFoot2d(Ped ped, float x1, float y1, float x2, float y2, float angle, bool sphere)`](lua/isCharInAngledAreaOnFoot2d.md) |
| [`bool result = isCharInAngledAreaInCar2d(Ped ped, float x1, float y1, float x2, float y2, float angle, bool sphere)`](lua/isCharInAngledAreaInCar2d.md) |
| [`bool result = isCharStoppedInAngledArea2d(Ped ped, float x1, float y1, float x2, float y2, float height, bool flag)`](lua/isCharStoppedInAngledArea2d.md) |
| [`bool result = isCharStoppedInAngledAreaOnFoot2d(Ped ped, float x1, float y1, float x2, float y2, float angle, bool sphere)`](lua/isCharStoppedInAngledAreaOnFoot2d.md) |
| [`bool result = isCharStoppedInAngledAreaInCar2d(Ped ped, float x1, float y1, float x2, float y2, float height, bool flag)`](lua/isCharStoppedInAngledAreaInCar2d.md) |
| [`bool result = isCharInAngledArea3d(Ped ped, float x1, float y1, float z1, float x2, float y2, float z2, float angle, bool sphere)`](lua/isCharInAngledArea3d.md) |
| [`bool result = isCharInAngledAreaOnFoot3d(Ped ped, float x1, float y1, float z1, float x2, float y2, float z2, float angle, bool sphere)`](lua/isCharInAngledAreaOnFoot3d.md) |
| [`bool result = isCharInAngledAreaInCar3d(Ped ped, float x1, float y1, float z1, float x2, float y2, float z2, float depth, bool flag)`](lua/isCharInAngledAreaInCar3d.md) |
| [`bool result = isCharStoppedInAngledArea3d(Ped ped, float x1, float y1, float z1, float x2, float y2, float z2, float depth, bool flag)`](lua/isCharStoppedInAngledArea3d.md) |
| [`bool result = isCharStoppedInAngledAreaOnFoot3d(Ped ped, float x1, float y1, float z1, float x2, float y2, float z2, float depth, bool flag)`](lua/isCharStoppedInAngledAreaOnFoot3d.md) |
| [`bool result = isCharStoppedInAngledAreaInCar3d(Ped ped, float x1, float y1, float z1, float x2, float y2, float z2, float depth, bool flag)`](lua/isCharStoppedInAngledAreaInCar3d.md) |
| [`bool result = isCharInTaxi(Ped ped)`](lua/isCharInTaxi.md) |
| [`taskGoToCoordAnyMeans(Ped ped, float toX, float toY, float toZ, int mode, Vehicle useCar)`](lua/taskGoToCoordAnyMeans.md) |
| [`float zAngle = getHeadingFromVector2d(float pX, float pY)`](lua/getHeadingFromVector2d.md) |
| [`taskPlayAnim(Ped ped, string animation, string IFP, float framedelta, bool loop, bool lockX, bool lockY, bool lockF, int time)`](lua/taskPlayAnim.md) |
| [`loadPathNodesInArea(float x1, float y1, float x2, float y2)`](lua/loadPathNodesInArea.md) |
| [`releasePathNodes()`](lua/releasePathNodes.md) |
| [`int maker = loadCharDecisionMaker(int type)`](lua/loadCharDecisionMaker.md) |
| [`setCharDecisionMaker(Ped ped, int maker)`](lua/setCharDecisionMaker.md) |
| [`setTextDropshadow(int shadow, int r, int g, int b, int a)`](lua/setTextDropshadow.md) |
| [`bool result = isPlaybackGoingOnForCar(Vehicle car)`](lua/isPlaybackGoingOnForCar.md) |
| [`setSenseRange(Ped ped, float accuracy)`](lua/setSenseRange.md) |
| [`bool result = isCharPlayingAnim(Ped ped, string animation)`](lua/isCharPlayingAnim.md) |
| [`setCharAnimPlayingFlag(Ped ped, string animation, bool flag)`](lua/setCharAnimPlayingFlag.md) |
| [`float time = getCharAnimCurrentTime(Ped ped, string animation)`](lua/getCharAnimCurrentTime.md) |
| [`setCharAnimCurrentTime(Ped ped, string animation, float time)`](lua/setCharAnimCurrentTime.md) |
| [`int task = openSequenceTask()`](lua/openSequenceTask.md) |
| [`closeSequenceTask(int task)`](lua/closeSequenceTask.md) |
| [`performSequenceTask(Ped ped, int task)`](lua/performSequenceTask.md) |
| [`setCharCollision(Ped ped, bool enable)`](lua/setCharCollision.md) |
| [`float totalTime = getCharAnimTotalTime(Ped ped, string animation)`](lua/getCharAnimTotalTime.md) |
| [`clearSequenceTask(int task)`](lua/clearSequenceTask.md) |
| [`int handle = addAttractor(float originX, float originY, float originZ, float zAngle, float unknownAngle, int taskSequence)`](lua/addAttractor.md) |
| [`clearAttractor(int handle)`](lua/clearAttractor.md) |
| [`Ped ped = createCharAtAttractor(int pedtype, Model modelId, int ASOrigin, int task)`](lua/createCharAtAttractor.md) |
| [`taskLeaveCarImmediately(Ped ped, Vehicle car)`](lua/taskLeaveCarImmediately.md) |
| [`incrementIntStat(int stat, int add)`](lua/incrementIntStat.md) |
| [`incrementFloatStat(int stat, float add)`](lua/incrementFloatStat.md) |
| [`decrementIntStat(int stat, int int)`](lua/decrementIntStat.md) |
| [`decrementFloatStat(int stat, float float)`](lua/decrementFloatStat.md) |
| [`registerIntStat(int stat, int int)`](lua/registerIntStat.md) |
| [`registerFloatStat(int stat, float value)`](lua/registerFloatStat.md) |
| [`setIntStat(int stat, int int)`](lua/setIntStat.md) |
| [`setFloatStat(int stat, float float)`](lua/setFloatStat.md) |
| [`int status = getScriptTaskStatus(Ped ped, int task)`](lua/getScriptTaskStatus.md) |
| [`int group = createGroup(int type)`](lua/createGroup.md) |
| [`setGroupLeader(int group, Ped ped)`](lua/setGroupLeader.md) |
| [`setGroupMember(int group, Ped ped)`](lua/setGroupMember.md) |
| [`removeGroup(int group)`](lua/removeGroup.md) |
| [`taskLeaveAnyCar(Ped ped)`](lua/taskLeaveAnyCar.md) |
| [`taskKillCharOnFootWhileDucking(Ped ped, int weapon, int flags, int time, int chance)`](lua/taskKillCharOnFootWhileDucking.md) |
| [`taskAimGunAtChar(Ped ped, int aimAt, int timeMS)`](lua/taskAimGunAtChar.md) |
| [`taskGoToCoordWhileShooting(Ped ped, float toX, float toY, float toZ, int mode, float turnRadius, float stopRadius, int lookAtActor)`](lua/taskGoToCoordWhileShooting.md) |
| [`taskStayInSamePlace(Ped ped, bool stay)`](lua/taskStayInSamePlace.md) |
| [`taskTurnCharToFaceChar(Ped ped, int rotateTo)`](lua/taskTurnCharToFaceChar.md) |
| [`bool result = isCharAtScriptedAttractor(Ped ped, int origin)`](lua/isCharAtScriptedAttractor.md) |
| [`setSequenceToRepeat(int pack, bool loop)`](lua/setSequenceToRepeat.md) |
| [`int progess = getSequenceProgress(Ped ped)`](lua/getSequenceProgress.md) |
| [`clearLookAt(Ped ped)`](lua/clearLookAt.md) |
| [`setFollowNodeThresholdDistance(Ped ped, float dist)`](lua/setFollowNodeThresholdDistance.md) |
| [`Particle particle = createFxSystem(string particle, float pX, float pY, float pZ, int type)`](lua/createFxSystem.md) |
| [`playFxSystem(Particle particle)`](lua/playFxSystem.md) |
| [`stopFxSystem(Particle particle)`](lua/stopFxSystem.md) |
| [`playAndKillFxSystem(Particle particle)`](lua/playAndKillFxSystem.md) |
| [`killFxSystem(Particle particle)`](lua/killFxSystem.md) |
| [`int stat = getIntStat(int stat)`](lua/getIntStat.md) |
| [`float stat = getFloatStat(int stat)`](lua/getFloatStat.md) |
| [`setObjectRenderScorched(Object object, bool fireproof)`](lua/setObjectRenderScorched.md) |
| [`taskLookAtObject(Ped ped, int lookAt, int timeMS)`](lua/taskLookAtObject.md) |
| [`float float = limitAngle(float angle)`](lua/limitAngle.md) |
| [`openCarDoor(Vehicle car, int door)`](lua/openCarDoor.md) |
| [`float X, float Y, float Z = getPickupCoordinates(Pickup pickup)`](lua/getPickupCoordinates.md) |
| [`removeDecisionMaker(int maker)`](lua/removeDecisionMaker.md) |
| [`Model modelId = getCharModel(Ped ped)`](lua/getCharModel.md) |
| [`taskAimGunAtCoord(Ped ped, float atX, float atY, float atZ, int timeMS)`](lua/taskAimGunAtCoord.md) |
| [`taskShootAtCoord(Ped ped, float atX, float atY, float atZ, int timeMS)`](lua/taskShootAtCoord.md) |
| [`Particle particle = createFxSystemOnChar(string particle, Ped ped, float offsetX, float offsetY, float offsetZ, int type)`](lua/createFxSystemOnChar.md) |
| [`Particle particle = createFxSystemOnCharWithDirection(string particle, Ped ped, float offsetX, float offsetY, float offsetZ, float rotationX, float rotationY, float rotationZ, int type)`](lua/createFxSystemOnCharWithDirection.md) |
| [`Particle particle = createFxSystemOnCar(string particle, Vehicle car, float offsetX, float offsetY, float offsetZ, int type)`](lua/createFxSystemOnCar.md) |
| [`Particle particle = createFxSystemOnCarWithDirection(string particle, Vehicle car, float offsetX, float offsetY, float offsetZ, float rotationX, float rotationY, float rotationZ, int type)`](lua/createFxSystemOnCarWithDirection.md) |
| [`Particle particle = createFxSystemOnObject(string particle, Object object, float offsetX, float offsetY, float offsetZ, int type)`](lua/createFxSystemOnObject.md) |
| [`Particle particle = createFxSystemOnObjectWithDirection(string particle, Object object, float offsetX, float offsetY, float offsetZ, float rotationX, float rotationY, float rotationZ, int flag)`](lua/createFxSystemOnObjectWithDirection.md) |
| [`taskDestroyCar(Ped ped, Vehicle car)`](lua/taskDestroyCar.md) |
| [`taskDiveAndGetUp(Ped ped, float toOffsetX, float toOffsetY, int time)`](lua/taskDiveAndGetUp.md) |
| [`customPlateForNextCar(Model modelId, string numberplate)`](lua/customPlateForNextCar.md) |
| [`taskShuffleToNextCarSeat(Ped ped, Vehicle car)`](lua/taskShuffleToNextCarSeat.md) |
| [`taskChatWithChar(Ped ped, int withActor, bool flag, int unknownFlag)`](lua/taskChatWithChar.md) |
| [`attachCameraToVehicle(Vehicle car, float offsetX, float offsetY, float offsetZ, float rotationX, float rotationY, float rotationZ, float tilt, int switchstyle)`](lua/attachCameraToVehicle.md) |
| [`attachCameraToVehicleLookAtVehicle(Vehicle car, float offsetX, float offsetY, float offsetZ, int toCar, float tilt, int switchstyle)`](lua/attachCameraToVehicleLookAtVehicle.md) |
| [`attachCameraToVehicleLookAtChar(Vehicle car, float offsetX, float offsetY, float offsetZ, Ped ped, float tilt, int switchstyle)`](lua/attachCameraToVehicleLookAtChar.md) |
| [`attachCameraToChar(Ped ped, float offsetX, float offsetY, float offsetZ, float rotationX, float rotationY, float rotationZ, float tilt, int switchstyle)`](lua/attachCameraToChar.md) |
| [`attachCameraToCharLookAtChar(Ped ped, float offsetX, float offsetY, float offsetZ, int targetActor, float tilt, int switchstyle)`](lua/attachCameraToCharLookAtChar.md) |
| [`forceCarLights(Vehicle car, int lights)`](lua/forceCarLights.md) |
| [`addPedtypeAsAttractorUser(int ASOrigin, int pedtype)`](lua/addPedtypeAsAttractorUser.md) |
| [`attachObjectToCar(Object object, Vehicle car, float offsetX, float offsetY, float offsetZ, float rotationX, float rotationY, float rotationZ)`](lua/attachObjectToCar.md) |
| [`detachObject(Object object, float X, float Y, float Z, bool collisionDetection)`](lua/detachObject.md) |
| [`attachCarToCar(Vehicle car, int toCar, float offsetX, float offsetY, float offsetZ, float rotationX, float rotationY, float rotationZ)`](lua/attachCarToCar.md) |
| [`detachCar(Vehicle car, float X, float Y, float Z, bool collisionDetection)`](lua/detachCar.md) |
| [`bool result = isObjectAttached(Object object)`](lua/isObjectAttached.md) |
| [`bool result = isVehicleAttached(Vehicle car)`](lua/isVehicleAttached.md) |
| [`clearCharTasks(Ped ped)`](lua/clearCharTasks.md) |
| [`taskTogglePedThreatScanner(Ped ped, bool unknownFlag1, bool unknownFlag2, bool unknownFlag3)`](lua/taskTogglePedThreatScanner.md) |
| [`popCarDoor(Vehicle car, int door, bool visible)`](lua/popCarDoor.md) |
| [`fixCarDoor(Vehicle car, int door)`](lua/fixCarDoor.md) |
| [`taskEveryoneLeaveCar(Vehicle car)`](lua/taskEveryoneLeaveCar.md) |
| [`bool result = isPlayerTargettingAnything(Player player)`](lua/isPlayerTargettingAnything.md) |
| [`float X, float Y, float Z = getActiveCameraCoordinates()`](lua/getActiveCameraCoordinates.md) |
| [`float X, float Y, float Z = getActiveCameraPointAt()`](lua/getActiveCameraPointAt.md) |
| [`popCarPanel(Vehicle car, int component, bool effectFlag)`](lua/popCarPanel.md) |
| [`fixCarPanel(Vehicle car, int componentB)`](lua/fixCarPanel.md) |
| [`fixCarTire(Vehicle car, int tire)`](lua/fixCarTire.md) |
| [`attachObjectToObject(Object object, int toObject, float offsetX, float offsetY, float offsetZ, float rotationX, float rotationY, float rotationZ)`](lua/attachObjectToObject.md) |
| [`attachObjectToChar(Object object, Ped ped, float offsetX, float offsetY, float offsetZ, float rotationX, float rotationY, float rotationZ)`](lua/attachObjectToChar.md) |
| [`float vecX, float vecY, float vecZ = getCarSpeedVector(Vehicle car)`](lua/getCarSpeedVector.md) |
| [`float mass = getCarMass(Vehicle car)`](lua/getCarMass.md) |
| [`taskDiveFromAttachmentAndGetUp(Ped ped, int timeMS)`](lua/taskDiveFromAttachmentAndGetUp.md) |
| [`attachCharToBike(Ped ped, Vehicle car, float offsetX, float offsetY, float offsetZ, int position, float shootingAngle1, float shootingAngle2, int weapon)`](lua/attachCharToBike.md) |
| [`taskGotoCharOffset(Ped ped, int toActor, int timelimit, float approachDistance, float approachAngle)`](lua/taskGotoCharOffset.md) |
| [`taskLookAtCoord(Ped ped, float toX, float toY, float toZ, int timeMS)`](lua/taskLookAtCoord.md) |
| [`hideCharWeaponForScriptedCutscene(Ped ped, bool hide)`](lua/hideCharWeaponForScriptedCutscene.md) |
| [`float speed = getCharSpeed(Ped ped)`](lua/getCharSpeed.md) |
| [`setGroupDecisionMaker(int group, int maker)`](lua/setGroupDecisionMaker.md) |
| [`int maker = loadGroupDecisionMaker(int type)`](lua/loadGroupDecisionMaker.md) |
| [`disablePlayerSprint(Player player, bool mode)`](lua/disablePlayerSprint.md) |
| [`taskSitDown(Ped ped, int timeMS)`](lua/taskSitDown.md) |
| [`Searchlight searchlight = createSearchlight(float atX, float atY, float atZ, float targetX, float targetY, float targetZ, float radius1, float radius2)`](lua/createSearchlight.md) |
| [`deleteSearchlight(Searchlight searchlight)`](lua/deleteSearchlight.md) |
| [`bool result = doesSearchlightExist(Searchlight searchlight)`](lua/doesSearchlightExist.md) |
| [`moveSearchlightBetweenCoords(Searchlight searchlight, float fromX, float fromY, float fromZ, float toX, float toY, float toZ, float speed)`](lua/moveSearchlightBetweenCoords.md) |
| [`pointSearchlightAtCoord(Searchlight searchlight, float toX, float toY, float toZ, float speed)`](lua/pointSearchlightAtCoord.md) |
| [`pointSearchlightAtChar(Searchlight searchlight, Ped ped, float speed)`](lua/pointSearchlightAtChar.md) |
| [`bool result = isCharInSearchlight(Searchlight searchlight, Ped ped)`](lua/isCharInSearchlight.md) |
| [`bool result = hasCutsceneLoaded()`](lua/hasCutsceneLoaded.md) |
| [`taskTurnCharToFaceCoord(Ped ped, float atX, float atY, float atZ)`](lua/taskTurnCharToFaceCoord.md) |
| [`taskDrivePointRoute(Ped ped, Vehicle car, float speed)`](lua/taskDrivePointRoute.md) |
| [`fireSingleBullet(float fromX, float fromY, float fromZ, float targetX, float targetY, float targetZ, int energy)`](lua/fireSingleBullet.md) |
| [`bool result = isLineOfSightClear(float fromX, float fromY, float fromZ, float toX, float toY, float toZ, bool checkBuildings, bool checkVehicles, bool checkActors, bool checkObjects, bool checkParticles)`](lua/isLineOfSightClear.md) |
| [`float roll = getCarRoll(Vehicle car)`](lua/getCarRoll.md) |
| [`pointSearchlightAtVehicle(Searchlight searchlight, Vehicle car, float speed)`](lua/pointSearchlightAtVehicle.md) |
| [`bool result = isVehicleInSearchlight(int int, Vehicle car)`](lua/isVehicleInSearchlight.md) |
| [`Searchlight searchlight = createSearchlightOnVehicle(Vehicle car, float offsetX, float offsetY, float offsetZ, float targetX, float targetY, float targetZ, float radius, float radius)`](lua/createSearchlightOnVehicle.md) |
| [`taskGoToCoordWhileAiming(Ped ped, float toX, float toY, float toZ, int mode, float turnRadius, float stopRadius, Ped ped, float offsetX, float offsetY, float offsetZ)`](lua/taskGoToCoordWhileAiming.md) |
| [`int num = getNumberOfFiresInRange(float atX, float atY, float atZ, float radius)`](lua/getNumberOfFiresInRange.md) |
| [`Marker marker = addBlipForSearchlight(Searchlight searchlight)`](lua/addBlipForSearchlight.md) |
| [`skipToEndAndStopPlaybackRecordedCar(Vehicle car)`](lua/skipToEndAndStopPlaybackRecordedCar.md) |
| [`taskCarTempAction(Ped ped, Vehicle car, int performAction, int timelimit)`](lua/taskCarTempAction.md) |
| [`setLaRiots(bool enable)`](lua/setLaRiots.md) |
| [`removeCharFromGroup(Ped ped)`](lua/removeCharFromGroup.md) |
| [`attachSearchlightToSearchlightObject(Searchlight searchlight, int tower, int housing, int bulb, float offsetX, float offsetY, float offsetZ)`](lua/attachSearchlightToSearchlightObject.md) |
| [`switchEmergencyServices(bool enable)`](lua/switchEmergencyServices.md) |
| [`Checkpoint checkpoint = createCheckpoint(int type, float atX, float atY, float atZ, float pointX, float pointY, float pointZ, float radius)`](lua/createCheckpoint.md) |
| [`deleteCheckpoint(Checkpoint checkpoint)`](lua/deleteCheckpoint.md) |
| [`switchRandomTrains(bool enable)`](lua/switchRandomTrains.md) |
| [`Vehicle train = createMissionTrain(int type, float atX, float atY, float atZ, bool direction)`](lua/createMissionTrain.md) |
| [`deleteMissionTrains()`](lua/deleteMissionTrains.md) |
| [`markMissionTrainsAsNoLongerNeeded()`](lua/markMissionTrainsAsNoLongerNeeded.md) |
| [`deleteAllTrains()`](lua/deleteAllTrains.md) |
| [`setTrainSpeed(Vehicle train, float speed)`](lua/setTrainSpeed.md) |
| [`setTrainCruiseSpeed(Vehicle train, float speed)`](lua/setTrainCruiseSpeed.md) |
| [`int caboose = getTrainCaboose(Vehicle train)`](lua/getTrainCaboose.md) |
| [`deletePlayer(Player player)`](lua/deletePlayer.md) |
| [`setTwoPlayerCameraMode(bool mode)`](lua/setTwoPlayerCameraMode.md) |
| [`taskCarMission(Ped ped, Vehicle car, int targetCar, int order, float maxSpeed, int trafficFlag)`](lua/taskCarMission.md) |
| [`taskGoToObject(Ped ped, int toObject, int timelimit, float stopWithinRadius)`](lua/taskGoToObject.md) |
| [`taskWeaponRoll(Ped ped, bool roll)`](lua/taskWeaponRoll.md) |
| [`taskCharArrestChar(Ped ped, int bustActor)`](lua/taskCharArrestChar.md) |
| [`Model itemID = getAvailableVehicleMod(Vehicle car, int poolIndex)`](lua/getAvailableVehicleMod.md) |
| [`int type = getVehicleModType(Model component)`](lua/getVehicleModType.md) |
| [`int componentId = addVehicleMod(Vehicle car, Model component)`](lua/addVehicleMod.md) |
| [`removeVehicleMod(Vehicle car, int componentId)`](lua/removeVehicleMod.md) |
| [`requestVehicleMod(Model component)`](lua/requestVehicleMod.md) |
| [`bool result = hasVehicleModLoaded(Model component)`](lua/hasVehicleModLoaded.md) |
| [`markVehicleModAsNoLongerNeeded(Model component)`](lua/markVehicleModAsNoLongerNeeded.md) |
| [`int num = getNumAvailablePaintjobs(Vehicle car)`](lua/getNumAvailablePaintjobs.md) |
| [`giveVehiclePaintjob(int set, int paintjob)`](lua/giveVehiclePaintjob.md) |
| [`bool result = isGroupMember(Ped ped, int group)`](lua/isGroupMember.md) |
| [`bool result = isGroupLeader(Ped ped, int group)`](lua/isGroupLeader.md) |
| [`setGroupSeparationRange(int group, float range)`](lua/setGroupSeparationRange.md) |
| [`limitTwoPlayerDistance(float distance)`](lua/limitTwoPlayerDistance.md) |
| [`releaseTwoPlayerDistance()`](lua/releaseTwoPlayerDistance.md) |
| [`setPlayerPlayerTargetting(bool can)`](lua/setPlayerPlayerTargetting.md) |
| [`float X, float Y, float Z = getScriptFireCoords(int fire)`](lua/getScriptFireCoords.md) |
| [`float X, float Y, float Z, float ZAngle = getNthClosestCarNodeWithHeading(float forX, float forY, float forZ, int direction)`](lua/getNthClosestCarNodeWithHeading.md) |
| [`setPlayersCanBeInSeparateCars(bool allow)`](lua/setPlayersCanBeInSeparateCars.md) |
| [`bool result = doesCarHaveStuckCarCheck(Vehicle car)`](lua/doesCarHaveStuckCarCheck.md) |
| [`setPlaybackSpeed(Vehicle car, float speed)`](lua/setPlaybackSpeed.md) |
| [`bool result = areAnyCharsNearChar(Ped ped, float range)`](lua/areAnyCharsNearChar.md) |
| [`skipCutsceneEnd()`](lua/skipCutsceneEnd.md) |
| [`int percentage = getPercentageTaggedInArea(float x1, float y1, float x2, float y2)`](lua/getPercentageTaggedInArea.md) |
| [`setTagStatusInArea(float x1, float y1, float x2, float y2, bool value)`](lua/setTagStatusInArea.md) |
| [`carGotoCoordinatesRacing(Vehicle car, float toX, float toY, float toZ)`](lua/carGotoCoordinatesRacing.md) |
| [`startPlaybackRecordedCarUsingAi(Vehicle car, int path)`](lua/startPlaybackRecordedCarUsingAi.md) |
| [`skipInPlaybackRecordedCar(Vehicle car, float path)`](lua/skipInPlaybackRecordedCar.md) |
| [`clearCharDecisionMakerEventResponse(int maker, int event)`](lua/clearCharDecisionMakerEventResponse.md) |
| [`addCharDecisionMakerEventResponse(int maker, int event, int taskID, float respect, float hate, float like, float dislike, bool inCar, bool onFoot)`](lua/addCharDecisionMakerEventResponse.md) |
| [`taskPickUpObject(Ped ped, Object object, float offsetX, float offsetY, float offsetZ, int boneId1, int boneId2, string performAnimation, int IFPFile, int time)`](lua/taskPickUpObject.md) |
| [`dropObject(Ped ped, bool object)`](lua/dropObject.md) |
| [`explodeCarInCutscene(Vehicle car)`](lua/explodeCarInCutscene.md) |
| [`buildPlayerModel(Player player)`](lua/buildPlayerModel.md) |
| [`planeAttackPlayer(int hydra, Vehicle car, float radius)`](lua/planeAttackPlayer.md) |
| [`planeFlyInDirection(int plane, float direction, float altitudemin, float altitudemax)`](lua/planeFlyInDirection.md) |
| [`planeFollowEntity(int plane, Ped ped, Vehicle car, float radius)`](lua/planeFollowEntity.md) |
| [`taskDriveBy(Ped ped, int drivebyActor, Vehicle car, float pX, float pY, float pZ, float radiusX, int radiusY, bool radiusZ, int firingRate)`](lua/taskDriveBy.md) |
| [`setCarStayInSlowLane(Vehicle car, bool stay)`](lua/setCarStayInSlowLane.md) |
| [`takeRemoteControlOfCar(Player player, Vehicle car)`](lua/takeRemoteControlOfCar.md) |
| [`bool result = isClosestObjectOfTypeSmashedOrDamaged(Model object, float atX, float atY, float atZ, float radius, bool smashed, bool damaged)`](lua/isClosestObjectOfTypeSmashedOrDamaged.md) |
| [`startSettingUpConversation(Ped ped)`](lua/startSettingUpConversation.md) |
| [`finishSettingUpConversation()`](lua/finishSettingUpConversation.md) |
| [`bool result = isConversationAtNode(Ped ped, GxtString gxtString)`](lua/isConversationAtNode.md) |
| [`int health = getObjectHealth(Object object)`](lua/getObjectHealth.md) |
| [`setObjectHealth(Object object, int health)`](lua/setObjectHealth.md) |
| [`breakObject(Object object, int intensity)`](lua/breakObject.md) |
| [`heliAttackPlayer(Vehicle heli, Player player, float radius)`](lua/heliAttackPlayer.md) |
| [`heliFollowEntity(Vehicle heli, Ped ped, Vehicle car, float radius)`](lua/heliFollowEntity.md) |
| [`policeHeliChaseEntity(Vehicle heli, Ped ped, Vehicle car, float radius)`](lua/policeHeliChaseEntity.md) |
| [`taskUseMobilePhone(Ped ped, bool hold)`](lua/taskUseMobilePhone.md) |
| [`taskWarpCharIntoCarAsDriver(Ped ped, Vehicle car)`](lua/taskWarpCharIntoCarAsDriver.md) |
| [`taskWarpCharIntoCarAsPassenger(Ped ped, Vehicle car, int passengerseat)`](lua/taskWarpCharIntoCarAsPassenger.md) |
| [`switchCopsOnBikes(bool generate)`](lua/switchCopsOnBikes.md) |
| [`bool result = isFlameInAngledArea2d(float x1, float y1, float x2, float y2, float angle, bool sphere)`](lua/isFlameInAngledArea2d.md) |
| [`bool result = isFlameInAngledArea3d(float x1, float y1, float z1, float x2, float y2, float z2, float angle, bool sphere)`](lua/isFlameInAngledArea3d.md) |
| [`addStuckCarCheckWithWarp(Vehicle car, float checkDistance, int time, bool stuck, bool flipped, bool warp, int path)`](lua/addStuckCarCheckWithWarp.md) |
| [`damageCarPanel(Vehicle car, int door)`](lua/damageCarPanel.md) |
| [`setCarRoll(Vehicle car, float roll)`](lua/setCarRoll.md) |
| [`bool result = suppressCarModel(Model modelId)`](lua/suppressCarModel.md) |
| [`dontSuppressCarModel(Model modelId)`](lua/dontSuppressCarModel.md) |
| [`dontSuppressAnyCarModels()`](lua/dontSuppressAnyCarModels.md) |
| [`bool result = isPs2KeyboardKeyPressed(int key)`](lua/isPs2KeyboardKeyPressed.md) |
| [`bool result = isPs2KeyboardKeyJustPressed(int key)`](lua/isPs2KeyboardKeyJustPressed.md) |
| [`bool result = isCharHoldingObject(Ped ped, int liftingObject)`](lua/isCharHoldingObject.md) |
| [`setCarCanGoAgainstTraffic(Vehicle car, bool can)`](lua/setCarCanGoAgainstTraffic.md) |
| [`damageCarDoor(Vehicle car, int door)`](lua/damageCarDoor.md) |
| [`Vehicle car = getRandomCarInSphereNoSave(float X, float Y, float Z, float radius, int model)`](lua/getRandomCarInSphereNoSave.md) |
| [`Ped ped = getRandomCharInSphere(float X, float Y, float Z, float radius, bool pedtypeCivilian, bool gang, bool prostitute)`](lua/getRandomCharInSphere.md) |
| [`bool result = hasCharBeenArrested(Ped ped)`](lua/hasCharBeenArrested.md) |
| [`setPlaneThrottle(int plane, float throttle)`](lua/setPlaneThrottle.md) |
| [`heliLandAtCoords(Vehicle heli, float X, float Y, float Z, float minaltitude, float maxaltitude)`](lua/heliLandAtCoords.md) |
| [`planeStartsInAir(int hydra)`](lua/planeStartsInAir.md) |
| [`setRelationship(int acquaintance, int pedtype, int toPedtype)`](lua/setRelationship.md) |
| [`clearRelationship(int acquaintance, int pedtype, int toPedtype)`](lua/clearRelationship.md) |
| [`clearGroupDecisionMakerEventResponse(int maker, int event)`](lua/clearGroupDecisionMakerEventResponse.md) |
| [`addGroupDecisionMakerEventResponse(int maker, int event, int taskID, float respect, float hate, float like, float dislike, bool inCar, bool onFoot)`](lua/addGroupDecisionMakerEventResponse.md) |
| [`drawSpriteWithRotation(int texture, float x, float y, float scaleX, float scaleY, float angle, int r, int g, int b, int a)`](lua/drawSpriteWithRotation.md) |
| [`taskUseAttractor(Ped ped, int attractor)`](lua/taskUseAttractor.md) |
| [`taskShootAtChar(Ped ped, int atActor, int timelimit)`](lua/taskShootAtChar.md) |
| [`setInformRespectedFriends(int flags, float radius, int pedsToScan)`](lua/setInformRespectedFriends.md) |
| [`bool result = isCharRespondingToEvent(Ped ped, int event)`](lua/isCharRespondingToEvent.md) |
| [`setObjectVisible(Object object, bool visibility)`](lua/setObjectVisible.md) |
| [`taskFleeCharAnyMeans(Ped ped, int fleeFrom, float runDistance, int time, bool changeCourse, int unkTime1, int unkTime2, float awayRadius)`](lua/taskFleeCharAnyMeans.md) |
| [`flushPatrolRoute()`](lua/flushPatrolRoute.md) |
| [`extendPatrolRoute(float X, float Y, float Z, string animation, string IFPFile)`](lua/extendPatrolRoute.md) |
| [`bool result = playObjectAnim(Object object, string animation, string IFPFile, float framedelta, bool lockF, bool loop)`](lua/playObjectAnim.md) |
| [`setRadarZoom(int zoom)`](lua/setRadarZoom.md) |
| [`bool result = doesBlipExist(Marker marker)`](lua/doesBlipExist.md) |
| [`loadPrices(GxtString shopping)`](lua/loadPrices.md) |
| [`loadShop(GxtString shopping)`](lua/loadShop.md) |
| [`int num = getNumberOfItemsInShop()`](lua/getNumberOfItemsInShop.md) |
| [`int item = getItemInShop(int index)`](lua/getItemInShop.md) |
| [`int price = getPriceOfItem(int item)`](lua/getPriceOfItem.md) |
| [`taskDead(Ped ped)`](lua/taskDead.md) |
| [`setCarAsMissionCar(Vehicle car)`](lua/setCarAsMissionCar.md) |
| [`setZonePopulationType(GxtString zone, int popcycle)`](lua/setZonePopulationType.md) |
| [`setZoneDealerStrength(GxtString zone, int density)`](lua/setZoneDealerStrength.md) |
| [`int strength = getZoneDealerStrength(GxtString zone)`](lua/getZoneDealerStrength.md) |
| [`setZoneGangStrength(GxtString zone, int gang, int density)`](lua/setZoneGangStrength.md) |
| [`int density = getZoneGangStrength(GxtString zone, int gang)`](lua/getZoneGangStrength.md) |
| [`bool result = isMessageBeingDisplayed()`](lua/isMessageBeingDisplayed.md) |
| [`setCharIsTargetPriority(Ped ped, bool targetPriority)`](lua/setCharIsTargetPriority.md) |
| [`customPlateDesignForNextCar(Model modelNumplate, int townTexture)`](lua/customPlateDesignForNextCar.md) |
| [`taskGotoCar(Ped ped, Vehicle car, int timeMS, float stopAtDistance)`](lua/taskGotoCar.md) |
| [`requestIpl(string group)`](lua/requestIpl.md) |
| [`removeIpl(string group)`](lua/removeIpl.md) |
| [`removeIplDiscreetly(string group)`](lua/removeIplDiscreetly.md) |
| [`setCharRelationship(Ped ped, int acquaintance, int pedtype)`](lua/setCharRelationship.md) |
| [`clearCharRelationship(Ped ped, int acquaintance, int pedtype)`](lua/clearCharRelationship.md) |
| [`clearAllCharRelationships(Ped ped, int acquaintance)`](lua/clearAllCharRelationships.md) |
| [`float pitch = getCarPitch(Vehicle car)`](lua/getCarPitch.md) |
| [`int interior = getActiveInterior()`](lua/getActiveInterior.md) |
| [`heliKeepEntityInView(Vehicle heli, Ped ped, Vehicle car, float minaltitude, float maxaltitude)`](lua/heliKeepEntityInView.md) |
| [`int model = getWeapontypeModel(int id)`](lua/getWeapontypeModel.md) |
| [`int slot = getWeapontypeSlot(int id)`](lua/getWeapontypeSlot.md) |
| [`int info = getShoppingExtraInfo(int item, int flag)`](lua/getShoppingExtraInfo.md) |
| [`givePlayerClothes(Player player, int texture, int model, int bodypart)`](lua/givePlayerClothes.md) |
| [`int num = getNumberOfFiresInArea(float x1, float y1, float z1, float x2, float y2, float z2)`](lua/getNumberOfFiresInArea.md) |
| [`attachWinchToHeli(Vehicle heli, bool magnet)`](lua/attachWinchToHeli.md) |
| [`releaseEntityFromWinch(Vehicle heli)`](lua/releaseEntityFromWinch.md) |
| [`int carriage = getTrainCarriage(Vehicle train, int handle)`](lua/getTrainCarriage.md) |
| [`Vehicle carHandle, Ped pedHandle, Object objectHandle = grabEntityOnWinch(Vehicle heli)`](lua/grabEntityOnWinch.md) |
| [`GxtString name = getNameOfItem(int item)`](lua/getNameOfItem.md) |
| [`taskClimb(Ped ped, bool climb)`](lua/taskClimb.md) |
| [`buyItem(int item)`](lua/buyItem.md) |
| [`clearCharTasksImmediately(Ped ped)`](lua/clearCharTasksImmediately.md) |
| [`storeClothesState()`](lua/storeClothesState.md) |
| [`restoreClothesState()`](lua/restoreClothesState.md) |
| [`float length = getRopeHeightForObject(int magnet)`](lua/getRopeHeightForObject.md) |
| [`setRopeHeightForObject(int magnet, float length)`](lua/setRopeHeightForObject.md) |
| [`Vehicle carHandle, Ped pedHandle, Object objectHandle = grabEntityOnRopeForObject(int magnet)`](lua/grabEntityOnRopeForObject.md) |
| [`releaseEntityFromRopeForObject(int magnet)`](lua/releaseEntityFromRopeForObject.md) |
| [`playerEnteredDockCrane()`](lua/playerEnteredDockCrane.md) |
| [`playerEnteredBuildingsiteCrane()`](lua/playerEnteredBuildingsiteCrane.md) |
| [`playerLeftCrane()`](lua/playerLeftCrane.md) |
| [`performSequenceTaskFromProgress(Ped ped, int sequence, int unkProgress1, int unkProgress2)`](lua/performSequenceTaskFromProgress.md) |
| [`setNextDesiredMoveState(int speed)`](lua/setNextDesiredMoveState.md) |
| [`taskGotoCharAiming(Ped ped, int followActor, float minradius, float maxradius)`](lua/taskGotoCharAiming.md) |
| [`int unkProgress1, int unkProgress2 = getSequenceProgressRecursive(Ped ped)`](lua/getSequenceProgressRecursive.md) |
| [`taskKillCharOnFootTimed(Ped ped, int attackActor, int time)`](lua/taskKillCharOnFootTimed.md) |
| [`float X, float Y, float Z = getNearestTagPosition(float X, float Y, float Z)`](lua/getNearestTagPosition.md) |
| [`taskJetpack(Ped ped)`](lua/taskJetpack.md) |
| [`setArea51SamSite(bool enable)`](lua/setArea51SamSite.md) |
| [`bool result, Searchlight searchlight = isCharInAnySearchlight(Ped ped)`](lua/isCharInAnySearchlight.md) |
| [`bool result = isTrailerAttachedToCab(Vehicle trailer, Vehicle car)`](lua/isTrailerAttachedToCab.md) |
| [`detachTrailerFromCab(Vehicle trailer, Vehicle cab)`](lua/detachTrailerFromCab.md) |
| [`int group = getPlayerGroup(Player player)`](lua/getPlayerGroup.md) |
| [`GxtString shop = getLoadedShop()`](lua/getLoadedShop.md) |
| [`int int2, int int3, int int4 = getBeatProximity(int track)`](lua/getBeatProximity.md) |
| [`setGroupDefaultTaskAllocator(int group, int command)`](lua/setGroupDefaultTaskAllocator.md) |
| [`setPlayerGroupRecruitment(Player player, bool enabled)`](lua/setPlayerGroupRecruitment.md) |
| [`activateHeliSpeedCheat(Vehicle heli, int power)`](lua/activateHeliSpeedCheat.md) |
| [`taskSetCharDecisionMaker(Ped ped, int maker)`](lua/taskSetCharDecisionMaker.md) |
| [`deleteMissionTrain(Vehicle train)`](lua/deleteMissionTrain.md) |
| [`markMissionTrainAsNoLongerNeeded(Vehicle train)`](lua/markMissionTrainAsNoLongerNeeded.md) |
| [`setBlipAlwaysDisplayOnZoomedRadar(Marker marker, bool displayAlways)`](lua/setBlipAlwaysDisplayOnZoomedRadar.md) |
| [`requestCarRecording(int path)`](lua/requestCarRecording.md) |
| [`bool result = hasCarRecordingBeenLoaded(int path)`](lua/hasCarRecordingBeenLoaded.md) |
| [`setMissionTrainCoordinates(Vehicle train, float X, float Y, float Z)`](lua/setMissionTrainCoordinates.md) |
| [`taskComplexPickupObject(Ped ped, Object object)`](lua/taskComplexPickupObject.md) |
| [`listenToPlayerGroupCommands(Ped ped, bool listen)`](lua/listenToPlayerGroupCommands.md) |
| [`setPlayerEnterCarButton(Player player, bool can)`](lua/setPlayerEnterCarButton.md) |
| [`taskCharSlideToCoord(Ped ped, float toX, float toY, float toZ, float angle, float withinRadius)`](lua/taskCharSlideToCoord.md) |
| [`int weekday = getCurrentDayOfWeek()`](lua/getCurrentDayOfWeek.md) |
| [`registerScriptBrainForCodeUse(int id, GxtString gxtString)`](lua/registerScriptBrainForCodeUse.md) |
| [`applyForceToCar(Vehicle car, float vecX, float vecY, float vecZ, float rotationX, float rotationY, float rotationZ)`](lua/applyForceToCar.md) |
| [`addToCarRotationVelocity(Vehicle car, float vecX, float vecY, float vecZ)`](lua/addToCarRotationVelocity.md) |
| [`setCarRotationVelocity(Vehicle car, float vecX, float vecY, float vecZ)`](lua/setCarRotationVelocity.md) |
| [`setCharShootRate(Ped ped, int rate)`](lua/setCharShootRate.md) |
| [`bool result = isModelInCdimage(Model modelId)`](lua/isModelInCdimage.md) |
| [`removeOilPuddlesInArea(float x1, float y1, float x2, float y2)`](lua/removeOilPuddlesInArea.md) |
| [`setBlipAsFriendly(Marker marker, bool type)`](lua/setBlipAsFriendly.md) |
| [`taskSwimToCoord(Ped ped, float toX, float toY, float toZ)`](lua/taskSwimToCoord.md) |
| [`float x1, float y1, float z1, float x2, float y2, float z2 = getModelDimensions(Model modelId)`](lua/getModelDimensions.md) |
| [`int maker = copyCharDecisionMaker(Ped ped)`](lua/copyCharDecisionMaker.md) |
| [`int maker = copyGroupDecisionMaker(int group)`](lua/copyGroupDecisionMaker.md) |
| [`taskDrivePointRouteAdvanced(Ped ped, Vehicle car, float speed, int flag1, int flag2, int flag3)`](lua/taskDrivePointRouteAdvanced.md) |
| [`bool result = isRelationshipSet(int acquaintance, int ofActors, int toActors)`](lua/isRelationshipSet.md) |
| [`setCarAlwaysCreateSkids(Vehicle car, bool enable)`](lua/setCarAlwaysCreateSkids.md) |
| [`int city = getCityFromCoords(float X, float Y, float Z)`](lua/getCityFromCoords.md) |
| [`bool result = hasObjectOfTypeBeenSmashed(float X, float Y, float Z, float radius, Model modelId)`](lua/hasObjectOfTypeBeenSmashed.md) |
| [`bool result = isPlayerPerformingWheelie(Player player)`](lua/isPlayerPerformingWheelie.md) |
| [`bool result = isPlayerPerformingStoppie(Player player)`](lua/isPlayerPerformingStoppie.md) |
| [`setCheckpointCoords(Checkpoint checkpoint, float X, float Y, float Z)`](lua/setCheckpointCoords.md) |
| [`controlCarHydraulics(Vehicle car, float f1, float f2, float f3, float f4)`](lua/controlCarHydraulics.md) |
| [`int numberOfLeaders, int numberOfMembers = getGroupSize(int group)`](lua/getGroupSize.md) |
| [`setObjectCollisionDamageEffect(Object object, bool destructible)`](lua/setObjectCollisionDamageEffect.md) |
| [`setCarFollowCar(Vehicle car, int followCar, float radius)`](lua/setCarFollowCar.md) |
| [`playerEnteredQuarryCrane()`](lua/playerEnteredQuarryCrane.md) |
| [`playerEnteredLasVegasCrane()`](lua/playerEnteredLasVegasCrane.md) |
| [`switchEntryExit(GxtString interior, bool access)`](lua/switchEntryExit.md) |
| [`displayTextWithFloat(float X, float Y, GxtString GXT, float value, int flag)`](lua/displayTextWithFloat.md) |
| [`bool result = doesGroupExist(int group)`](lua/doesGroupExist.md) |
| [`giveMeleeAttackToChar(Ped ped, int fightingStyle, int moves)`](lua/giveMeleeAttackToChar.md) |
| [`setCarHydraulics(Vehicle car, bool hydraulics)`](lua/setCarHydraulics.md) |
| [`bool result = is2playerGameGoingOn()`](lua/is2playerGameGoingOn.md) |
| [`float fov = getCameraFov()`](lua/getCameraFov.md) |
| [`bool result = doesCarHaveHydraulics(Vehicle car)`](lua/doesCarHaveHydraulics.md) |
| [`taskCharSlideToCoordAndPlayAnim(Ped ped, float toX, float toY, float toZ, float angle, float radius, string animation, int ifp1, float ifp2, bool LA, bool LX, bool LY, bool LF, int LT)`](lua/taskCharSlideToCoordAndPlayAnim.md) |
| [`int number = getTotalNumberOfPedsKilledByPlayer(Player player)`](lua/getTotalNumberOfPedsKilledByPlayer.md) |
| [`float X, float Y, float Z = getLevelDesignCoordsForObject(Object object, int spoot)`](lua/getLevelDesignCoordsForObject.md) |
| [`int event = getCharHighestPriorityEvent(Ped ped)`](lua/getCharHighestPriorityEvent.md) |
| [`float X, float Y, float Z = getParkingNodeInArea(float x1, float y1, float z1, float x2, float y2, float z2)`](lua/getParkingNodeInArea.md) |
| [`Vehicle car = getCarCharIsUsing(Ped ped)`](lua/getCarCharIsUsing.md) |
| [`taskPlayAnimNonInterruptable(Ped ped, string animation, string IFP, float framedelta, bool loopA, bool lockX, bool lockY, bool lockF, int time)`](lua/taskPlayAnimNonInterruptable.md) |
| [`addStuntJump(float startX, float startY, float startZ, float radiusX, float radiusY, float radiusZ, float goalX, float goalY, float goalZ, float radius2X, float radius2Y, float radius2Z, float cameraX, float cameraY, float cameraZ, int reward)`](lua/addStuntJump.md) |
| [`setObjectCoordinatesAndVelocity(Object object, float X, float Y, float Z)`](lua/setObjectCoordinatesAndVelocity.md) |
| [`setCharKindaStayInSamePlace(Ped ped, bool stay)`](lua/setCharKindaStayInSamePlace.md) |
| [`taskFollowPatrolRoute(Ped ped, int walkMode, int routeMode)`](lua/taskFollowPatrolRoute.md) |
| [`bool result = isCharInAir(Ped ped)`](lua/isCharInAir.md) |
| [`float height = getCharHeightAboveGround(Ped ped)`](lua/getCharHeightAboveGround.md) |
| [`setCharWeaponSkill(Ped ped, int skill)`](lua/setCharWeaponSkill.md) |
| [`setTextEdge(int size, int r, int g, int b, int a)`](lua/setTextEdge.md) |
| [`setCarEngineBroken(Vehicle car, bool broken)`](lua/setCarEngineBroken.md) |
| [`bool result = isThisModelABoat(Model modelId)`](lua/isThisModelABoat.md) |
| [`bool result = isThisModelAPlane(Model modelId)`](lua/isThisModelAPlane.md) |
| [`bool result = isThisModelAHeli(Model modelId)`](lua/isThisModelAHeli.md) |
| [`setFirstPersonInCarCameraMode(bool enable)`](lua/setFirstPersonInCarCameraMode.md) |
| [`taskGreetPartner(Ped ped, Ped ped2, float unk1, int unk2)`](lua/taskGreetPartner.md) |
| [`setHeliBladesFullSpeed(Vehicle heli)`](lua/setHeliBladesFullSpeed.md) |
| [`displayHud(bool enable)`](lua/displayHud.md) |
| [`connectLods(Object object, int lod)`](lua/connectLods.md) |
| [`setMaxFireGenerations(int max)`](lua/setMaxFireGenerations.md) |
| [`taskDieNamedAnim(Ped ped, string animation, string ifp1, float ifp2, int time)`](lua/taskDieNamedAnim.md) |
| [`setPlayerDuckButton(Player player, bool able)`](lua/setPlayerDuckButton.md) |
| [`setPoolTableCoords(float x1, float y1, float z1, float x2, float y2, float z2)`](lua/setPoolTableCoords.md) |
| [`bool result = hasObjectBeenPhotographed(Object object)`](lua/hasObjectBeenPhotographed.md) |
| [`doCameraBump(float rotationZ, float rotationY)`](lua/doCameraBump.md) |
| [`int day, int month = getCurrentDate()`](lua/getCurrentDate.md) |
| [`setObjectAnimSpeed(Object object, string animation, float speed)`](lua/setObjectAnimSpeed.md) |
| [`bool result = isObjectPlayingAnim(Object object, string anim)`](lua/isObjectPlayingAnim.md) |
| [`float progress = getObjectAnimCurrentTime(Object object, string animation)`](lua/getObjectAnimCurrentTime.md) |
| [`setObjectAnimCurrentTime(Object object, string animation, float progress)`](lua/setObjectAnimCurrentTime.md) |
| [`setCharVelocity(Ped ped, float vecX, float vecY, float vecZ)`](lua/setCharVelocity.md) |
| [`float vecX, float vecY, float vecZ = getCharVelocity(Ped ped)`](lua/getCharVelocity.md) |
| [`setCharRotation(Ped ped, float vecX, float vecY, float vecZ)`](lua/setCharRotation.md) |
| [`float value = getCarUprightValue(Vehicle car)`](lua/getCarUprightValue.md) |
| [`setVehicleInterior(Vehicle car, int interior)`](lua/setVehicleInterior.md) |
| [`selectWeaponsForVehicle(Vehicle car, bool gun)`](lua/selectWeaponsForVehicle.md) |
| [`int city = getCityPlayerIsIn(Player player)`](lua/getCityPlayerIsIn.md) |
| [`GxtString name = getNameOfZone(float X, float Y, float Z)`](lua/getNameOfZone.md) |
| [`activateInteriorPeds(bool activate)`](lua/activateInteriorPeds.md) |
| [`setVehicleCanBeTargetted(Vehicle car, bool unk)`](lua/setVehicleCanBeTargetted.md) |
| [`taskFollowFootsteps(Ped ped, int followActor)`](lua/taskFollowFootsteps.md) |
| [`damageChar(Ped ped, int health, bool affectArmour)`](lua/damageChar.md) |
| [`setCarCanBeVisiblyDamaged(Vehicle car, bool can)`](lua/setCarCanBeVisiblyDamaged.md) |
| [`setHeliReachedTargetDistance(Vehicle heli, int dist)`](lua/setHeliReachedTargetDistance.md) |
| [`float level = getSoundLevelAtCoords(Ped ped, float X, float Y, float Z)`](lua/getSoundLevelAtCoords.md) |
| [`setCharAllowedToDuck(Ped ped, bool enable)`](lua/setCharAllowedToDuck.md) |
| [`setHeadingForAttachedPlayer(Player player, float toAngle, float rotationSpeed)`](lua/setHeadingForAttachedPlayer.md) |
| [`taskWalkAlongsideChar(Ped ped, int alongisdeActor)`](lua/taskWalkAlongsideChar.md) |
| [`createEmergencyServicesCar(Model car, float X, float Y, float Z)`](lua/createEmergencyServicesCar.md) |
| [`taskKindaStayInSamePlace(Ped ped, bool stay)`](lua/taskKindaStayInSamePlace.md) |
| [`startPlaybackRecordedCarLooped(Vehicle car, int path)`](lua/startPlaybackRecordedCarLooped.md) |
| [`setCharInterior(Ped ped, int interior)`](lua/setCharInterior.md) |
| [`bool result = isAttachedPlayerHeadingAchieved(Player player)`](lua/isAttachedPlayerHeadingAchieved.md) |
| [`enableEntryExitPlayerGroupWarping(float X, float Y, float radius, bool access)`](lua/enableEntryExitPlayerGroupWarping.md) |
| [`Object object = getClosestStealableObject(float X, float Y, float Z, float radius)`](lua/getClosestStealableObject.md) |
| [`bool result = isProceduralInteriorActive(int interior)`](lua/isProceduralInteriorActive.md) |
| [`removeCarRecording(int path)`](lua/removeCarRecording.md) |
| [`setZonePopulationRace(GxtString zone, int popcycle)`](lua/setZonePopulationRace.md) |
| [`setObjectOnlyDamagedByPlayer(Object object, bool player)`](lua/setObjectOnlyDamagedByPlayer.md) |
| [`createBirds(float x1, float y1, float z1, float x2, float y2, float z2, int flag1, int flag2)`](lua/createBirds.md) |
| [`setVehicleDirtLevel(Vehicle car, float level)`](lua/setVehicleDirtLevel.md) |
| [`setGangWarsActive(bool enable)`](lua/setGangWarsActive.md) |
| [`bool result = isGangWarGoingOn()`](lua/isGangWarGoingOn.md) |
| [`givePlayerClothesOutsideShop(Player player, string clothes, string model, int bodyPart)`](lua/givePlayerClothesOutsideShop.md) |
| [`clearLoadedShop()`](lua/clearLoadedShop.md) |
| [`setGroupSequence(int group, int Aspack)`](lua/setGroupSequence.md) |
| [`setCharDropsWeaponsWhenDead(Ped ped, bool droppable)`](lua/setCharDropsWeaponsWhenDead.md) |
| [`setCharNeverLeavesGroup(Ped ped, bool set)`](lua/setCharNeverLeavesGroup.md) |
| [`setPlayerFireButton(Player player, bool able)`](lua/setPlayerFireButton.md) |
| [`attachFxSystemToCharBone(Particle particle, Ped ped, int mode)`](lua/attachFxSystemToCharBone.md) |
| [`registerAttractorScriptBrainForCodeUse(int handle, GxtString script)`](lua/registerAttractorScriptBrainForCodeUse.md) |
| [`setHeadingLimitForAttachedChar(Ped ped, int orientation, float limit)`](lua/setHeadingLimitForAttachedChar.md) |
| [`Marker blip = addBlipForDeadChar(Ped ped)`](lua/addBlipForDeadChar.md) |
| [`float X, float Y, float Z = getDeadCharCoordinates(Ped ped)`](lua/getDeadCharCoordinates.md) |
| [`taskPlayAnimWithFlags(Ped ped, string animation, string ifp, float framedelta, bool loopA, bool lockX, bool lockY, bool lockF, int time, bool force, bool lockZ)`](lua/taskPlayAnimWithFlags.md) |
| [`setVehicleAirResistanceMultiplier(Vehicle car, float multiplier)`](lua/setVehicleAirResistanceMultiplier.md) |
| [`setCarCoordinatesNoOffset(Vehicle car, float X, float Y, float Z)`](lua/setCarCoordinatesNoOffset.md) |
| [`setUsesCollisionOfClosestObjectOfType(float X, float Y, float Z, float radius, Model modelId, bool collisionDetection)`](lua/setUsesCollisionOfClosestObjectOfType.md) |
| [`setTimeOneDayForward()`](lua/setTimeOneDayForward.md) |
| [`setTimerBeepCountdownTime(VarId timer, int reach)`](lua/setTimerBeepCountdownTime.md) |
| [`attachTrailerToCab(int trailer, int cab)`](lua/attachTrailerToCab.md) |
| [`bool result = isVehicleTouchingObject(Vehicle car, Object object)`](lua/isVehicleTouchingObject.md) |
| [`enableCraneControls(bool UP, bool DOWN, bool RELEASE)`](lua/enableCraneControls.md) |
| [`bool result = isPlayerInPositionForConversation(Ped ped)`](lua/isPlayerInPositionForConversation.md) |
| [`enableConversation(Ped ped, bool enable)`](lua/enableConversation.md) |
| [`Ped ped = getRandomCharInSphereOnlyDrugsBuyers(float X, float Y, float Z, float radius)`](lua/getRandomCharInSphereOnlyDrugsBuyers.md) |
| [`int pedtype = getPedType(Ped ped)`](lua/getPedType.md) |
| [`bool result = taskUseClosestMapAttractor(Ped ped, float radius, Model nearModel, float offsetX, float offsetY, float offsetZ, string scriptNamed)`](lua/taskUseClosestMapAttractor.md) |
| [`planeAttackPlayerUsingDogFight(int hydra, Player player, float radius)`](lua/planeAttackPlayerUsingDogFight.md) |
| [`canTriggerGangWarWhenOnAMission(bool can)`](lua/canTriggerGangWarWhenOnAMission.md) |
| [`controlMovableVehiclePart(Vehicle car, float angle)`](lua/controlMovableVehiclePart.md) |
| [`winchCanPickVehicleUp(Vehicle car, bool attractive)`](lua/winchCanPickVehicleUp.md) |
| [`openCarDoorABit(Vehicle car, int door, float rotation)`](lua/openCarDoorABit.md) |
| [`bool result = isCarDoorFullyOpen(Vehicle car, int door)`](lua/isCarDoorFullyOpen.md) |
| [`setAlwaysDraw3dMarkers(bool set)`](lua/setAlwaysDraw3dMarkers.md) |
| [`streamScript(int script)`](lua/streamScript.md) |
| [`bool result = hasStreamedScriptLoaded(int script)`](lua/hasStreamedScriptLoaded.md) |
| [`setGangWarsTrainingMission(bool set)`](lua/setGangWarsTrainingMission.md) |
| [`setCharHasUsedEntryExit(Ped ped, float X, float Y, float radius)`](lua/setCharHasUsedEntryExit.md) |
| [`setCharMaxHealth(Ped ped, int health)`](lua/setCharMaxHealth.md) |
| [`setNightVision(bool enable)`](lua/setNightVision.md) |
| [`setInfraredVision(bool enable)`](lua/setInfraredVision.md) |
| [`setZoneForGangWarsTraining(GxtString zone)`](lua/setZoneForGangWarsTraining.md) |
| [`setCharCanBeKnockedOffBike(Ped ped, bool can)`](lua/setCharCanBeKnockedOffBike.md) |
| [`setCharCoordinatesDontWarpGang(Ped ped, float X, float Y, float Z)`](lua/setCharCoordinatesDontWarpGang.md) |
| [`addPriceModifier(int item, int price)`](lua/addPriceModifier.md) |
| [`removePriceModifier(int item)`](lua/removePriceModifier.md) |
| [`initZonePopulationSettings()`](lua/initZonePopulationSettings.md) |
| [`explodeCarInCutsceneShakeAndBits(Vehicle car, bool shake, bool effect, bool sound)`](lua/explodeCarInCutsceneShakeAndBits.md) |
| [`bool result = isSkipCutsceneButtonPressed()`](lua/isSkipCutsceneButtonPressed.md) |
| [`bool result, float X, float Y, float Z = getCutsceneOffset()`](lua/getCutsceneOffset.md) |
| [`setObjectScale(Object object, float scale)`](lua/setObjectScale.md) |
| [`int popcycle = getCurrentPopulationZoneType()`](lua/getCurrentPopulationZoneType.md) |
| [`int menu = createMenu(GxtString title, float posX, float posY, float width, int columns, bool interactive, bool background, int alignment)`](lua/createMenu.md) |
| [`setMenuColumnOrientation(int menu, int column, int alignment)`](lua/setMenuColumnOrientation.md) |
| [`int item = getMenuItemSelected(int menu)`](lua/getMenuItemSelected.md) |
| [`int item = getMenuItemAccepted(int menu)`](lua/getMenuItemAccepted.md) |
| [`activateMenuItem(int menu, int row, bool enable)`](lua/activateMenuItem.md) |
| [`deleteMenu(int menu)`](lua/deleteMenu.md) |
| [`setMenuColumn(int menu, int column, GxtString header, GxtString data1, GxtString data2, GxtString data3, GxtString data4, GxtString data5, GxtString data6, GxtString data7, GxtString data8, GxtString data9, GxtString data10, GxtString data11, GxtString data12)`](lua/setMenuColumn.md) |
| [`setBlipEntryExit(Marker marker, float X, float Y, float radius)`](lua/setBlipEntryExit.md) |
| [`switchDeathPenalties(bool lose)`](lua/switchDeathPenalties.md) |
| [`switchArrestPenalties(bool lose)`](lua/switchArrestPenalties.md) |
| [`setExtraHospitalRestartPoint(float X, float Y, float Z, float radius, float angle)`](lua/setExtraHospitalRestartPoint.md) |
| [`setExtraPoliceStationRestartPoint(float X, float Y, float Z, float radius, float angle)`](lua/setExtraPoliceStationRestartPoint.md) |
| [`int num = findNumberTagsTagged()`](lua/findNumberTagsTagged.md) |
| [`int percentage = getTerritoryUnderControlPercentage()`](lua/getTerritoryUnderControlPercentage.md) |
| [`bool result = isObjectInAngledArea2d(Object object, float x1, float y1, float x2, float y2, float radius, bool sphere)`](lua/isObjectInAngledArea2d.md) |
| [`bool result = isObjectInAngledArea3d(Object object, float x1, float y1, float z1, float x2, float y2, float z2, float depth, bool flag)`](lua/isObjectInAngledArea3d.md) |
| [`Ped ped = getRandomCharInSphereNoBrain(float X, float Y, float Z, float radius)`](lua/getRandomCharInSphereNoBrain.md) |
| [`setPlaneUndercarriageUp(int plane, bool set)`](lua/setPlaneUndercarriageUp.md) |
| [`disableAllEntryExits(bool disable)`](lua/disableAllEntryExits.md) |
| [`attachAnimsToModel(Model modelId, GxtString externalScript)`](lua/attachAnimsToModel.md) |
| [`setObjectAsStealable(Object object, bool liftable)`](lua/setObjectAsStealable.md) |
| [`setCreateRandomGangMembers(bool enable)`](lua/setCreateRandomGangMembers.md) |
| [`addSparks(float posX, float posY, float posZ, float vecX, float vecY, float vecZ, int density)`](lua/addSparks.md) |
| [`int class = getVehicleClass(Vehicle car)`](lua/getVehicleClass.md) |
| [`clearConversationForChar(Ped ped)`](lua/clearConversationForChar.md) |
| [`setMenuItemWithNumber(int panel, int column, int row, GxtString gxtString, int number)`](lua/setMenuItemWithNumber.md) |
| [`setMenuItemWith2Numbers(int panel, int column, int row, GxtString gxtString, int numbers1, int numbers2)`](lua/setMenuItemWith2Numbers.md) |
| [`setCutsceneModelTexture(GxtString cutsceneModel, GxtString textureName)`](lua/setCutsceneModelTexture.md) |
| [`GxtString nameB = getNameOfInfoZone(float atX, float atY, float atZ)`](lua/getNameOfInfoZone.md) |
| [`vehicleCanBeTargettedByHsMissile(Vehicle car, bool targetable)`](lua/vehicleCanBeTargettedByHsMissile.md) |
| [`setFreebiesInVehicle(Vehicle car, bool containsGoodies)`](lua/setFreebiesInVehicle.md) |
| [`setScriptLimitToGangSize(bool max)`](lua/setScriptLimitToGangSize.md) |
| [`makePlayerGangDisappear()`](lua/makePlayerGangDisappear.md) |
| [`makePlayerGangReappear()`](lua/makePlayerGangReappear.md) |
| [`int textureCRC, int modelCRC = getClothesItem(Player player, int bodypart)`](lua/getClothesItem.md) |
| [`showUpdateStats(bool display)`](lua/showUpdateStats.md) |
| [`setCoordBlipAppearance(Checkpoint checkpoint, int type)`](lua/setCoordBlipAppearance.md) |
| [`setHeathazeEffect(bool enable)`](lua/setHeathazeEffect.md) |
| [`bool result = isHelpMessageBeingDisplayed()`](lua/isHelpMessageBeingDisplayed.md) |
| [`bool result = hasObjectBeenDamagedByWeapon(Object object, int type)`](lua/hasObjectBeenDamagedByWeapon.md) |
| [`clearObjectLastWeaponDamage(Object object)`](lua/clearObjectLastWeaponDamage.md) |
| [`setPlayerJumpButton(Player player, bool enable)`](lua/setPlayerJumpButton.md) |
| [`int r, int g, int b, int a = getHudColour(int interface)`](lua/getHudColour.md) |
| [`lockDoor(int door, bool lock)`](lua/lockDoor.md) |
| [`setObjectMass(Object object, float mass)`](lua/setObjectMass.md) |
| [`float mass = getObjectMass(int int)`](lua/getObjectMass.md) |
| [`setObjectTurnMass(Object object, float turnMass)`](lua/setObjectTurnMass.md) |
| [`float turnMass = getObjectTurnMass(Object object)`](lua/getObjectTurnMass.md) |
| [`setSpecificZoneToTriggerGangWar(GxtString zone)`](lua/setSpecificZoneToTriggerGangWar.md) |
| [`clearSpecificZonesToTriggerGangWar()`](lua/clearSpecificZonesToTriggerGangWar.md) |
| [`setActiveMenuItem(int panel, int activeRow)`](lua/setActiveMenuItem.md) |
| [`markStreamedScriptAsNoLongerNeeded(int externalScript)`](lua/markStreamedScriptAsNoLongerNeeded.md) |
| [`removeStreamedScript(int externalScript)`](lua/removeStreamedScript.md) |
| [`setMessageFormatting(bool priority, int leftmargin, int maxwidth)`](lua/setMessageFormatting.md) |
| [`startNewStreamedScript(int externalScript, table args)`](lua/startNewStreamedScript.md) |
| [`setWeatherToAppropriateTypeNow()`](lua/setWeatherToAppropriateTypeNow.md) |
| [`winchCanPickObjectUp(Object object, bool enable)`](lua/winchCanPickObjectUp.md) |
| [`switchAudioZone(GxtString zone, bool enableSound)`](lua/switchAudioZone.md) |
| [`setCarEngineOn(Vehicle car, bool on)`](lua/setCarEngineOn.md) |
| [`setCarLightsOn(Vehicle car, bool lights)`](lua/setCarLightsOn.md) |
| [`Ped ped = getUserOfClosestMapAttractor(float sphereX, float sphereY, float sphereZ, float radius, Model modelId, string externalScriptNamed)`](lua/getUserOfClosestMapAttractor.md) |
| [`switchRoadsBackToOriginal(float cornerAX, float cornerAY, float cornerAZ, float cornerBX, float cornerBY, float cornerBZ)`](lua/switchRoadsBackToOriginal.md) |
| [`switchPedRoadsBackToOriginal(float cornerAX, float cornerAY, float cornerAZ, float cornerBX, float cornerBY, float cornerBZ)`](lua/switchPedRoadsBackToOriginal.md) |
| [`int landingGearStatus = getPlaneUndercarriagePosition(int plane)`](lua/getPlaneUndercarriagePosition.md) |
| [`cameraSetVectorTrack(float pointX, float pointY, float pointZ, float transverseX, float transverseY, float transverseZ, int time, bool smooth)`](lua/cameraSetVectorTrack.md) |
| [`cameraSetLerpFov(float from, float to, int timelimit, bool smoothTransition)`](lua/cameraSetLerpFov.md) |
| [`switchAmbientPlanes(bool enable)`](lua/switchAmbientPlanes.md) |
| [`setDarknessEffect(bool enable, int value)`](lua/setDarknessEffect.md) |
| [`cameraResetNewScriptables()`](lua/cameraResetNewScriptables.md) |
| [`int value = getNumberOfInstancesOfStreamedScript(int externalScript)`](lua/getNumberOfInstancesOfStreamedScript.md) |
| [`allocateStreamedScriptToRandomPed(int externalScript, Model actorModel, int priority)`](lua/allocateStreamedScriptToRandomPed.md) |
| [`allocateStreamedScriptToObject(int externalScript, Model objectModel, int priority, float radius, int type)`](lua/allocateStreamedScriptToObject.md) |
| [`int handle = getGroupMember(int group, int member)`](lua/getGroupMember.md) |
| [`float height = getWaterHeightAtCoords(float atX, float atY, bool ignoreWaves)`](lua/getWaterHeightAtCoords.md) |
| [`cameraPersistTrack(bool lock)`](lua/cameraPersistTrack.md) |
| [`cameraPersistPos(bool lock)`](lua/cameraPersistPos.md) |
| [`cameraPersistFov(bool lock)`](lua/cameraPersistFov.md) |
| [`bool result = cameraIsVectorMoveRunning()`](lua/cameraIsVectorMoveRunning.md) |
| [`bool result = cameraIsVectorTrackRunning()`](lua/cameraIsVectorTrackRunning.md) |
| [`cameraSetVectorMove(float cameraX, float cameraY, float cameraZ, float positionX, float positionY, float positionZ, int time, bool smoothTransition)`](lua/cameraSetVectorMove.md) |
| [`drawWindow(float cornerAX, float cornerAY, float cornerBX, float cornerBY, GxtString gxtString, int style)`](lua/drawWindow.md) |
| [`attachCarToObject(Vehicle car, Object object, float offsetX, float offsetY, float offsetZ, float rotationX, float rotationY, float rotationZ)`](lua/attachCarToObject.md) |
| [`setGarageResprayFree(GxtString garage, bool free)`](lua/setGarageResprayFree.md) |
| [`setCharBulletproofVest(Ped ped, bool enable)`](lua/setCharBulletproofVest.md) |
| [`setCinemaCamera(bool lock)`](lua/setCinemaCamera.md) |
| [`setCharFireDamageMultiplier(Ped ped, float multiplier)`](lua/setCharFireDamageMultiplier.md) |
| [`setGroupFollowStatus(int group, bool status)`](lua/setGroupFollowStatus.md) |
| [`setSearchlightClipIfColliding(Searchlight searchlight, bool flag)`](lua/setSearchlightClipIfColliding.md) |
| [`bool result = hasPlayerBoughtItem(int item)`](lua/hasPlayerBoughtItem.md) |
| [`setCameraInFrontOfChar(Ped ped)`](lua/setCameraInFrontOfChar.md) |
| [`int maxArmour = getPlayerMaxArmour(Player player)`](lua/getPlayerMaxArmour.md) |
| [`setCharUsesUpperbodyDamageAnimsOnly(Ped ped, bool uninterupted)`](lua/setCharUsesUpperbodyDamageAnimsOnly.md) |
| [`int spokenPhrase = setCharSayContext(Ped ped, int speech)`](lua/setCharSayContext.md) |
| [`addExplosionVariableShake(float atX, float atY, float atZ, int type, float cameraShake)`](lua/addExplosionVariableShake.md) |
| [`attachMissionAudioToChar(int id, Ped ped)`](lua/attachMissionAudioToChar.md) |
| [`updatePickupMoneyPerDay(Pickup pickup, int cash)`](lua/updatePickupMoneyPerDay.md) |
| [`GxtString interiorName = getNameOfEntryExitCharUsed(Ped ped)`](lua/getNameOfEntryExitCharUsed.md) |
| [`float coordX, float coordY, float coordZ, int number = getPositionOfEntryExitCharUsed(Ped ped)`](lua/getPositionOfEntryExitCharUsed.md) |
| [`bool result = isCharTalking(Ped ped)`](lua/isCharTalking.md) |
| [`disableCharSpeech(Ped ped, bool disable)`](lua/disableCharSpeech.md) |
| [`enableCharSpeech(Ped ped)`](lua/enableCharSpeech.md) |
| [`setUpSkip(float posX, float posY, float posZ, float angle)`](lua/setUpSkip.md) |
| [`clearSkip()`](lua/clearSkip.md) |
| [`preloadBeatTrack(int soundtrack)`](lua/preloadBeatTrack.md) |
| [`int status = getBeatTrackStatus()`](lua/getBeatTrackStatus.md) |
| [`playBeatTrack()`](lua/playBeatTrack.md) |
| [`stopBeatTrack()`](lua/stopBeatTrack.md) |
| [`int max = findMaxNumberOfGroupMembers()`](lua/findMaxNumberOfGroupMembers.md) |
| [`vehicleDoesProvideCover(Vehicle car, bool providesCover)`](lua/vehicleDoesProvideCover.md) |
| [`Pickup pickup = createSnapshotPickup(float atX, float atY, float atZ)`](lua/createSnapshotPickup.md) |
| [`Pickup pickup = createHorseshoePickup(float atX, float atY, float atZ)`](lua/createHorseshoePickup.md) |
| [`Pickup pickup = createOysterPickup(float atX, float atY, float atZ)`](lua/createOysterPickup.md) |
| [`bool result = hasObjectBeenUprooted(Object object)`](lua/hasObjectBeenUprooted.md) |
| [`addSmokeParticle(float atX, float atY, float atZ, float velocityX, float velocityY, float velocityZ, int r, int g, int b, int a, float size, float factor)`](lua/addSmokeParticle.md) |
| [`bool result = isCharStuckUnderCar(Ped ped)`](lua/isCharStuckUnderCar.md) |
| [`controlCarDoor(Vehicle car, int door, int unlatch, float angle)`](lua/controlCarDoor.md) |
| [`float angle = getDoorAngleRatio(Vehicle car, int door)`](lua/getDoorAngleRatio.md) |
| [`setPlayerDisplayVitalStatsButton(Player player, bool display)`](lua/setPlayerDisplayVitalStatsButton.md) |
| [`setCharKeepTask(Ped ped, bool keepTasks)`](lua/setCharKeepTask.md) |
| [`int id = createMenuGrid(GxtString gxtString, int positionX, int positionY, float width, int columns, bool interactive, bool background, int alignment)`](lua/createMenuGrid.md) |
| [`bool result = isCharSwimming(Ped ped)`](lua/isCharSwimming.md) |
| [`int status = getCharSwimState(Ped ped)`](lua/getCharSwimState.md) |
| [`startCharFacialTalk(Ped ped, int time)`](lua/startCharFacialTalk.md) |
| [`stopCharFacialTalk(Ped ped)`](lua/stopCharFacialTalk.md) |
| [`bool result = isBigVehicle(Vehicle car)`](lua/isBigVehicle.md) |
| [`switchPoliceHelis(bool enable)`](lua/switchPoliceHelis.md) |
| [`storeCarModState()`](lua/storeCarModState.md) |
| [`restoreCarModState()`](lua/restoreCarModState.md) |
| [`Model modelId = getCurrentCarMod(Vehicle car, int slot)`](lua/getCurrentCarMod.md) |
| [`bool result = isCarLowRider(Vehicle car)`](lua/isCarLowRider.md) |
| [`bool result = isCarStreetRacer(Vehicle car)`](lua/isCarStreetRacer.md) |
| [`forceDeathRestart()`](lua/forceDeathRestart.md) |
| [`syncWater()`](lua/syncWater.md) |
| [`setCharCoordinatesNoOffset(Ped ped, float atX, float atY, float atZ)`](lua/setCharCoordinatesNoOffset.md) |
| [`bool result = doesScriptFireExist(int fire)`](lua/doesScriptFireExist.md) |
| [`resetStuffUponResurrection()`](lua/resetStuffUponResurrection.md) |
| [`bool result = isEmergencyServicesVehicle(Vehicle car)`](lua/isEmergencyServicesVehicle.md) |
| [`killFxSystemNow(Particle particle)`](lua/killFxSystemNow.md) |
| [`bool result = isObjectWithinBrainActivationRange(Player player)`](lua/isObjectWithinBrainActivationRange.md) |
| [`int to = copySharedCharDecisionMaker(int from)`](lua/copySharedCharDecisionMaker.md) |
| [`reportMissionAudioEventAtPosition(float atX, float atY, float atZ, int event)`](lua/reportMissionAudioEventAtPosition.md) |
| [`reportMissionAudioEventAtObject(int at, int event)`](lua/reportMissionAudioEventAtObject.md) |
| [`attachMissionAudioToObject(int id, Object object)`](lua/attachMissionAudioToObject.md) |
| [`int colours = getNumCarColours(Vehicle car)`](lua/getNumCarColours.md) |
| [`extinguishFireAtPoint(float atX, float atY, float atZ, float radius)`](lua/extinguishFireAtPoint.md) |
| [`bool result = hasTrainDerailed(Vehicle train)`](lua/hasTrainDerailed.md) |
| [`setCharForceDieInCar(Ped ped, bool stayInCarWhenDead)`](lua/setCharForceDieInCar.md) |
| [`setOnlyCreateGangMembers(bool enable)`](lua/setOnlyCreateGangMembers.md) |
| [`Model modelId = getObjectModel(Object object)`](lua/getObjectModel.md) |
| [`setCharUsesCollisionClosestObjectOfType(float sphereX, float sphereY, float sphereZ, float radius, Model modelId, bool solid, int forActor)`](lua/setCharUsesCollisionClosestObjectOfType.md) |
| [`clearAllScriptFireFlags()`](lua/clearAllScriptFireFlags.md) |
| [`int blockingCar = getCarBlockingCar(Vehicle car)`](lua/getCarBlockingCar.md) |
| [`int paintjob = getCurrentVehiclePaintjob(Vehicle car)`](lua/getCurrentVehiclePaintjob.md) |
| [`setHelpMessageBoxSize(int width)`](lua/setHelpMessageBoxSize.md) |
| [`setGunshotSenseRangeForRiot2(float range)`](lua/setGunshotSenseRangeForRiot2.md) |
| [`float angle = getCarMovingComponentOffset(Vehicle car)`](lua/getCarMovingComponentOffset.md) |
| [`setNamedEntryExitFlag(GxtString interior, int bitmask, bool flag)`](lua/setNamedEntryExitFlag.md) |
| [`pauseCurrentBeatTrack(bool paused)`](lua/pauseCurrentBeatTrack.md) |
| [`setPlayerWeaponsScrollable(Player player, bool scrollable)`](lua/setPlayerWeaponsScrollable.md) |
| [`markRoadNodeAsDontWander(float atX, float atY, float atZ)`](lua/markRoadNodeAsDontWander.md) |
| [`unmarkAllRoadNodesAsDontWander()`](lua/unmarkAllRoadNodesAsDontWander.md) |
| [`setCheckpointHeading(Checkpoint checkpoint, float angle)`](lua/setCheckpointHeading.md) |
| [`setMissionRespectTotal(int respect)`](lua/setMissionRespectTotal.md) |
| [`awardPlayerMissionRespect(int respect)`](lua/awardPlayerMissionRespect.md) |
| [`setCarCollision(Vehicle car, bool collision)`](lua/setCarCollision.md) |
| [`changePlaybackToUseAi(Vehicle car)`](lua/changePlaybackToUseAi.md) |
| [`cameraSetShakeSimulationSimple(int type, float timelimit, float intensity)`](lua/cameraSetShakeSimulationSimple.md) |
| [`bool result = isNightVisionActive()`](lua/isNightVisionActive.md) |
| [`setCreateRandomCops(bool enable)`](lua/setCreateRandomCops.md) |
| [`taskSetIgnoreWeaponRangeFlag(Ped ped, bool ignore)`](lua/taskSetIgnoreWeaponRangeFlag.md) |
| [`taskPickUpSecondObject(Ped ped, Object object, float offsetX, float offsetY, float offsetZ, int bone, int int7, string animation, string file, int time)`](lua/taskPickUpSecondObject.md) |
| [`dropSecondObject(Ped ped, bool to)`](lua/dropSecondObject.md) |
| [`removeObjectElegantly(Object object)`](lua/removeObjectElegantly.md) |
| [`drawCrosshair(bool draw)`](lua/drawCrosshair.md) |
| [`setUpConversationNodeWithSpeech(GxtString question, GxtString answerY, GxtString answerN, int questionWav, int answerYWav, int answerNWav)`](lua/setUpConversationNodeWithSpeech.md) |
| [`showBlipsOnAllLevels(bool enable)`](lua/showBlipsOnAllLevels.md) |
| [`setCharDruggedUp(Ped ped, bool druggedUp)`](lua/setCharDruggedUp.md) |
| [`bool result = isCharHeadMissing(Ped ped)`](lua/isCharHeadMissing.md) |
| [`int CRC32 = getHashKey(string string)`](lua/getHashKey.md) |
| [`setUpConversationEndNodeWithSpeech(GxtString gxtString, int speech)`](lua/setUpConversationEndNodeWithSpeech.md) |
| [`randomPassengerSay(int passengers, int audioTable)`](lua/randomPassengerSay.md) |
| [`hideAllFrontendBlips(bool hide)`](lua/hideAllFrontendBlips.md) |
| [`setPlayerInCarCameraMode(int mode)`](lua/setPlayerInCarCameraMode.md) |
| [`bool result = isCharInAnyTrain(Ped ped)`](lua/isCharInAnyTrain.md) |
| [`setUpSkipAfterMission(float posX, float posY, float posZ, float angle)`](lua/setUpSkipAfterMission.md) |
| [`setVehicleIsConsideredByPlayer(Vehicle car, bool accessible)`](lua/setVehicleIsConsideredByPlayer.md) |
| [`Model modelId, int class = getRandomCarModelInMemory(bool unk)`](lua/getRandomCarModelInMemory.md) |
| [`int doorStatus = getCarDoorLockStatus(Vehicle car)`](lua/getCarDoorLockStatus.md) |
| [`setClosestEntryExitFlag(float atX, float atY, float radius, int bitmask, bool flag)`](lua/setClosestEntryExitFlag.md) |
| [`setCharSignalAfterKill(Ped ped, bool signal)`](lua/setCharSignalAfterKill.md) |
| [`setCharWantedByPolice(Ped ped, bool wanted)`](lua/setCharWantedByPolice.md) |
| [`setZoneNoCops(GxtString zone, bool disableCops)`](lua/setZoneNoCops.md) |
| [`addBlood(float atX, float atY, float atZ, float offsetX, float offsetY, float offsetZ, int density, int onActor)`](lua/addBlood.md) |
| [`displayCarNames(bool show)`](lua/displayCarNames.md) |
| [`displayZoneNames(bool show)`](lua/displayZoneNames.md) |
| [`bool result = isCarDoorDamaged(Vehicle car, int door)`](lua/isCarDoorDamaged.md) |
| [`setCharCoordinatesDontWarpGangNoOffset(Ped ped, float atX, float atY, float atZ)`](lua/setCharCoordinatesDontWarpGangNoOffset.md) |
| [`setMinigameInProgress(bool enable)`](lua/setMinigameInProgress.md) |
| [`bool result = isMinigameInProgress()`](lua/isMinigameInProgress.md) |
| [`setForceRandomCarModel(Model modelId)`](lua/setForceRandomCarModel.md) |
| [`Vehicle car = getRandomCarOfTypeInAngledAreaNoSave(float x1, float y1, float x2, float y2, float angle, int int6)`](lua/getRandomCarOfTypeInAngledAreaNoSave.md) |
| [`addNextMessageToPreviousBriefs(bool int1)`](lua/addNextMessageToPreviousBriefs.md) |
| [`failKillFrenzy()`](lua/failKillFrenzy.md) |
| [`bool result = isCopVehicleInArea3dNoSave(float cornerAX, float cornerAY, float cornerAZ, float cornerBX, float cornerBY, float cornerBZ)`](lua/isCopVehicleInArea3dNoSave.md) |
| [`setPetrolTankWeakpoint(Vehicle car, bool enabled)`](lua/setPetrolTankWeakpoint.md) |
| [`bool result = isCharUsingMapAttractor(Ped ped)`](lua/isCharUsingMapAttractor.md) |
| [`setPlayerModel(Player player, Model modelId)`](lua/setPlayerModel.md) |
| [`bool result = areSubtitlesSwitchedOn()`](lua/areSubtitlesSwitchedOn.md) |
| [`removeCharFromCarMaintainPosition(Ped ped, Vehicle car)`](lua/removeCharFromCarMaintainPosition.md) |
| [`setObjectProofs(Object object, bool BP, bool FP, bool EP, bool CP, bool MP)`](lua/setObjectProofs.md) |
| [`bool result = isCarTouchingCar(Vehicle car1, Vehicle car2)`](lua/isCarTouchingCar.md) |
| [`bool result = doesObjectHaveThisModel(Object object, Model modelId)`](lua/doesObjectHaveThisModel.md) |
| [`setTrainForcedToSlowDown(Vehicle train, bool forced)`](lua/setTrainForcedToSlowDown.md) |
| [`bool result = isVehicleOnAllWheels(Vehicle car)`](lua/isVehicleOnAllWheels.md) |
| [`bool result = doesPickupExist(Pickup pickup)`](lua/doesPickupExist.md) |
| [`enableAmbientCrime(bool enable)`](lua/enableAmbientCrime.md) |
| [`clearWantedLevelInGarage()`](lua/clearWantedLevelInGarage.md) |
| [`int unk = setCharSayContextImportant(Ped ped, int soundslot, bool flags1, bool flags2, bool flags3)`](lua/setCharSayContextImportant.md) |
| [`setCharSayScript(Ped ped, int sound, bool flags1, bool flags2, bool flags3)`](lua/setCharSayScript.md) |
| [`forceInteriorLightingForPlayer(Player player, bool force)`](lua/forceInteriorLightingForPlayer.md) |
| [`useDetonator()`](lua/useDetonator.md) |
| [`bool result = isMoneyPickupAtCoords(float atX, float atY, float atZ)`](lua/isMoneyPickupAtCoords.md) |
| [`setMenuColumnWidth(int panel, int column, int width)`](lua/setMenuColumnWidth.md) |
| [`makeRoomInPlayerGangForMissionPeds(int group)`](lua/makeRoomInPlayerGangForMissionPeds.md) |
| [`bool result = isCharGettingInToACar(Ped ped)`](lua/isCharGettingInToACar.md) |
| [`setUpSkipForSpecificVehicle(float posX, float posY, float posZ, float angle, Vehicle car)`](lua/setUpSkipForSpecificVehicle.md) |
| [`int price = getCarModelValue(Model modelId)`](lua/getCarModelValue.md) |
| [`int generator = createCarGeneratorWithPlate(float atX, float atY, float atZ, float angle, Model modelId, int color1, int color2, bool forceSpawn, int alarm, int doorLock, int minDelay, int maxDelay, string plate)`](lua/createCarGeneratorWithPlate.md) |
| [`bool result = findTrainDirection(Vehicle train)`](lua/findTrainDirection.md) |
| [`setAircraftCarrierSamSite(bool enable)`](lua/setAircraftCarrierSamSite.md) |
| [`drawLightWithRange(float atX, float atY, float atZ, int r, int g, int b, float radius)`](lua/drawLightWithRange.md) |
| [`enableBurglaryHouses(bool enable)`](lua/enableBurglaryHouses.md) |
| [`bool result = isPlayerControlOn(Player player)`](lua/isPlayerControlOn.md) |
| [`int interior = getCharActiveInterior(Ped ped)`](lua/getCharActiveInterior.md) |
| [`giveNonPlayerCarNitro(Vehicle car)`](lua/giveNonPlayerCarNitro.md) |
| [`playerTakeOffGoggles(Player player, bool useAnim)`](lua/playerTakeOffGoggles.md) |
| [`allowFixedCameraCollision(bool allow)`](lua/allowFixedCameraCollision.md) |
| [`bool result = hasCharSpottedCharInFront(Ped ped, Ped ped2)`](lua/hasCharSpottedCharInFront.md) |
| [`forceBigMessageAndCounter(bool stayOnScreen)`](lua/forceBigMessageAndCounter.md) |
| [`setVehicleCameraTweak(Model carModel, float distance, float altitudeMultiplier, float angleX)`](lua/setVehicleCameraTweak.md) |
| [`resetVehicleCameraTweak()`](lua/resetVehicleCameraTweak.md) |
| [`reportMissionAudioEventAtChar(Ped ped, int event)`](lua/reportMissionAudioEventAtChar.md) |
| [`bool result = doesDecisionMakerExist(int maker)`](lua/doesDecisionMakerExist.md) |
| [`ignoreHeightDifferenceFollowingNodes(Ped ped, bool ignore)`](lua/ignoreHeightDifferenceFollowingNodes.md) |
| [`shutAllCharsUp(bool enable)`](lua/shutAllCharsUp.md) |
| [`setCharGetOutUpsideDownCar(Ped ped, bool canGetOut)`](lua/setCharGetOutUpsideDownCar.md) |
| [`reportMissionAudioEventAtCar(Vehicle car, int event)`](lua/reportMissionAudioEventAtCar.md) |
| [`doWeaponStuffAtStartOf2pGame()`](lua/doWeaponStuffAtStartOf2pGame.md) |
| [`bool result = hasGameJustReturnedFromFrontend()`](lua/hasGameJustReturnedFromFrontend.md) |
| [`int language = getCurrentLanguage()`](lua/getCurrentLanguage.md) |
| [`bool result = isObjectIntersectingWorld(Object object)`](lua/isObjectIntersectingWorld.md) |
| [`int width = getStringWidth(GxtString gxtString)`](lua/getStringWidth.md) |
| [`resetVehicleHydraulics(Vehicle car)`](lua/resetVehicleHydraulics.md) |
| [`setRespawnPointForDurationOfMission(float posX, float posY, float posZ)`](lua/setRespawnPointForDurationOfMission.md) |
| [`bool result = isThisModelACar(Model modelId)`](lua/isThisModelACar.md) |
| [`switchOnGroundSearchlight(Searchlight searchlight, bool lightsThroughObstacles)`](lua/switchOnGroundSearchlight.md) |
| [`bool result = isGangWarFightingGoingOn()`](lua/isGangWarFightingGoingOn.md) |
| [`bool result = isNextStationAllowed(Vehicle train)`](lua/isNextStationAllowed.md) |
| [`skipToNextAllowedStation(Vehicle train)`](lua/skipToNextAllowedStation.md) |
| [`int width = getStringWidthWithNumber(GxtString gxtString, int number)`](lua/getStringWidthWithNumber.md) |
| [`shutCharUpForScriptedSpeech(Ped ped, bool muted)`](lua/shutCharUpForScriptedSpeech.md) |
| [`enableDisabledAttractorsOnObject(Object object, bool enable)`](lua/enableDisabledAttractorsOnObject.md) |
| [`loadSceneInDirection(float coordX, float coordY, float coordZ, float angle)`](lua/loadSceneInDirection.md) |
| [`bool result = isPlayerUsingJetpack(Player player)`](lua/isPlayerUsingJetpack.md) |
| [`clearThisPrintBigNow(int style)`](lua/clearThisPrintBigNow.md) |
| [`bool result = hasLanguageChanged()`](lua/hasLanguageChanged.md) |
| [`incrementIntStatNoMessage(int stat, int value)`](lua/incrementIntStatNoMessage.md) |
| [`setExtraCarColours(Vehicle car, int tertiaryColor, int quaternaryColor)`](lua/setExtraCarColours.md) |
| [`int tertiaryColor, int quaternaryColor = getExtraCarColours(Vehicle car)`](lua/getExtraCarColours.md) |
| [`manageAllPopulation()`](lua/manageAllPopulation.md) |
| [`setNoResprays(bool enable)`](lua/setNoResprays.md) |
| [`bool result = hasCarBeenResprayed(Vehicle car)`](lua/hasCarBeenResprayed.md) |
| [`attachMissionAudioToCar(int audioId, Vehicle car)`](lua/attachMissionAudioToCar.md) |
| [`setHasBeenOwnedForCarGenerator(int generator, bool owned)`](lua/setHasBeenOwnedForCarGenerator.md) |
| [`setUpConversationNodeWithScriptedSpeech(GxtString questionGXT, GxtString answerYesGXT, GxtString answerNoGXT, int questionWAV, int answerYesWAV, int answerNoWAV)`](lua/setUpConversationNodeWithScriptedSpeech.md) |
| [`setAreaName(GxtString gxtString)`](lua/setAreaName.md) |
| [`taskPlayAnimSecondary(Ped ped, string animation, string IFP, float framedelta, bool loopA, bool lockX, bool lockY, bool lockF, int time)`](lua/taskPlayAnimSecondary.md) |
| [`bool result = isCharTouchingChar(Ped ped, Ped ped2)`](lua/isCharTouchingChar.md) |
| [`disableHeliAudio(Vehicle helicopter, bool disable)`](lua/disableHeliAudio.md) |
| [`taskHandGesture(Ped ped, Ped ped2)`](lua/taskHandGesture.md) |
| [`takePhoto(bool unk)`](lua/takePhoto.md) |
| [`incrementFloatStatNoMessage(int stat, float value)`](lua/incrementFloatStatNoMessage.md) |
| [`setPlayerGroupToFollowAlways(Player player, bool followAlways)`](lua/setPlayerGroupToFollowAlways.md) |
| [`improveCarByCheating(Vehicle car, bool affectedByCheats)`](lua/improveCarByCheating.md) |
| [`changeCarColourFromMenu(int panelID, Vehicle car, int colorslot, int activeRow)`](lua/changeCarColourFromMenu.md) |
| [`highlightMenuItem(int panel, int row, bool highlight)`](lua/highlightMenuItem.md) |
| [`setDisableMilitaryZones(bool disable)`](lua/setDisableMilitaryZones.md) |
| [`setCameraPositionUnfixed(float xAngle, float zAngle)`](lua/setCameraPositionUnfixed.md) |
| [`setRadioToPlayersFavouriteStation()`](lua/setRadioToPlayersFavouriteStation.md) |
| [`setDeathWeaponsPersist(Ped ped, bool persist)`](lua/setDeathWeaponsPersist.md) |
| [`setCharSwimSpeed(Ped ped, float speed)`](lua/setCharSwimSpeed.md) |
| [`bool result = isPlayerClimbing(Player player)`](lua/isPlayerClimbing.md) |
| [`bool result = isThisHelpMessageBeingDisplayed(GxtString gxtString)`](lua/isThisHelpMessageBeingDisplayed.md) |
| [`bool result = isWidescreenOnInOptions()`](lua/isWidescreenOnInOptions.md) |
| [`drawSubtitlesBeforeFade(bool flag)`](lua/drawSubtitlesBeforeFade.md) |
| [`drawOddjobTitleBeforeFade(bool flag)`](lua/drawOddjobTitleBeforeFade.md) |
| [`taskFollowPathNodesToCoordWithRadius(Ped ped, float toX, float toY, float toZ, int mode, int time, float stopRadius)`](lua/taskFollowPathNodesToCoordWithRadius.md) |
| [`setPhotoCameraEffect(bool firstPersonView)`](lua/setPhotoCameraEffect.md) |
| [`fixCar(Vehicle car)`](lua/fixCar.md) |
| [`setPlayerGroupToFollowNever(Player player, bool neverFollow)`](lua/setPlayerGroupToFollowNever.md) |
| [`bool result = isCharAttachedToAnyCar(Ped ped)`](lua/isCharAttachedToAnyCar.md) |
| [`Ped ped = storeCarCharIsAttachedToNoSave(Vehicle car)`](lua/storeCarCharIsAttachedToNoSave.md) |
| [`setUpSkipForVehicleFinishedByScript(float posX, float posY, float posZ, float angle, Vehicle car)`](lua/setUpSkipForVehicleFinishedByScript.md) |
| [`bool result = isSkipWaitingForScriptToFadeIn()`](lua/isSkipWaitingForScriptToFadeIn.md) |
| [`forceAllVehicleLightsOff(bool off)`](lua/forceAllVehicleLightsOff.md) |
| [`int mode = getPlayerInCarCameraMode()`](lua/getPlayerInCarCameraMode.md) |
| [`bool result = isLastBuildingModelShotByPlayer(Player player, Model modelId)`](lua/isLastBuildingModelShotByPlayer.md) |
| [`clearLastBuildingModelShotByPlayer(Player player)`](lua/clearLastBuildingModelShotByPlayer.md) |
| [`setUpConversationEndNodeWithScriptedSpeech(GxtString dialogueGxt, int wav)`](lua/setUpConversationEndNodeWithScriptedSpeech.md) |
| [`activatePimpCheat(bool enable)`](lua/activatePimpCheat.md) |
| [`Ped ped = getRandomCharInAreaOffsetNoSave(float sphereX, float sphereY, float sphereZ, float radiusX, float radiusY, float radiusZ)`](lua/getRandomCharInAreaOffsetNoSave.md) |
| [`setScriptCoopGame(bool enable)`](lua/setScriptCoopGame.md) |
| [`Marker marker = createUser3dMarker(float atX, float atY, float atZ, int color)`](lua/createUser3dMarker.md) |
| [`removeUser3dMarker(Marker marker)`](lua/removeUser3dMarker.md) |
| [`getRidOfPlayerProstitute()`](lua/getRidOfPlayerProstitute.md) |
| [`displayNonMinigameHelpMessages(bool display)`](lua/displayNonMinigameHelpMessages.md) |
| [`setRailtrackResistanceMult(float tracksFriction)`](lua/setRailtrackResistanceMult.md) |
| [`switchObjectBrains(int externalScript, bool canBeStreamedIn)`](lua/switchObjectBrains.md) |
| [`finishSettingUpConversationNoSubtitles()`](lua/finishSettingUpConversationNoSubtitles.md) |
| [`allowPauseInWidescreen(bool enable)`](lua/allowPauseInWidescreen.md) |
| [`float x, float y = getPcMouseMovement()`](lua/getPcMouseMovement.md) |
| [`bool result = isPcUsingJoypad()`](lua/isPcUsingJoypad.md) |
| [`bool result = isMouseUsingVerticalInversion()`](lua/isMouseUsingVerticalInversion.md) |
| [`bool result = startNewCustomScript(zstring filepath, table args)`](lua/startNewCustomScript.md) |
| [`launchCustomMission(zstring filepath, table args)`](lua/launchCustomMission.md) |
| [`int handle = getScmThreadStructNamed(GxtString thread)`](lua/getScmThreadStructNamed.md) |
| [`setCleoSharedVar(int var, int value)`](lua/setCleoSharedVar.md) |
| [`int value = getCleoSharedVar(int var)`](lua/getCleoSharedVar.md) |
| [`sampSpawnPlayer()`](lua/sampSpawnPlayer.md) |
| [`uint handle = sampGetBase()`](lua/sampGetBase.md) |
| [`sampAddChatMessage(zstring text, uint color)`](lua/sampAddChatMessage.md) |
| [`sampSendChat(zstring text)`](lua/sampSendChat.md) |
| [`bool result = isSampAvailable()`](lua/isSampAvailable.md) |
| [`sampRequestClass(int class)`](lua/sampRequestClass.md) |
| [`sampSendScmEvent(int event, int id, int param1, int param2)`](lua/sampSendScmEvent.md) |
| [`sampSetSpecialAction(int action)`](lua/sampSetSpecialAction.md) |
| [`sampSendDeathByPlayer(int playerId, int reason)`](lua/sampSendDeathByPlayer.md) |
| [`bool result, Vehicle car = sampGetCarHandleBySampVehicleId(int id)`](lua/sampGetCarHandleBySampVehicleId.md) |
| [`bool result, Ped ped = sampGetCharHandleBySampPlayerId(int id)`](lua/sampGetCharHandleBySampPlayerId.md) |
| [`bool result = sampIsChatInputActive()`](lua/sampIsChatInputActive.md) |
| [`sampSetSendrate(int type, int rate)`](lua/sampSetSendrate.md) |
| [`bool result = sampIsPlayerConnected(int id)`](lua/sampIsPlayerConnected.md) |
| [`uint structPtr = sampGetPlayerStructPtr(int id)`](lua/sampGetPlayerStructPtr.md) |
| [`int health = sampGetPlayerHealth(int id)`](lua/sampGetPlayerHealth.md) |
| [`int armor = sampGetPlayerArmor(int id)`](lua/sampGetPlayerArmor.md) |
| [`sampSetGamestate(int gamestate)`](lua/sampSetGamestate.md) |
| [`sampDisconnectWithReason(bool timeout)`](lua/sampDisconnectWithReason.md) |
| [`sampSetLocalPlayerName(zstring name)`](lua/sampSetLocalPlayerName.md) |
| [`int ping = sampGetPlayerPing(int id)`](lua/sampGetPlayerPing.md) |
| [`bool result, int id = sampGetPlayerIdByCharHandle(Ped ped)`](lua/sampGetPlayerIdByCharHandle.md) |
| [`bool result, int id = sampGetVehicleIdByCarHandle(Vehicle car)`](lua/sampGetVehicleIdByCarHandle.md) |
| [`bool result, float posX, float posY, float posZ = sampGetStreamedOutPlayerPos(int id)`](lua/sampGetStreamedOutPlayerPos.md) |
| [`sampSendEnterVehicle(int id, bool passenger)`](lua/sampSendEnterVehicle.md) |
| [`sampSendExitVehicle(int id)`](lua/sampSendExitVehicle.md) |
| [`sampSendSpawn()`](lua/sampSendSpawn.md) |
| [`sampSendDamageVehicle(Vehicle car, int panel, int doors, int lights, int tires)`](lua/sampSendDamageVehicle.md) |
| [`bool result = sampRegisterChatCommand(zstring cmd, function func)`](lua/sampRegisterChatCommand.md) |
| [`zstring name = sampGetPlayerNickname(int id)`](lua/sampGetPlayerNickname.md) |
| [`uint color = sampGetPlayerColor(int id)`](lua/sampGetPlayerColor.md) |
| [`sampConnectToServer(zstring ip, uint port)`](lua/sampConnectToServer.md) |
| [`zstring ip, uint port = sampGetCurrentServerAddress()`](lua/sampGetCurrentServerAddress.md) |
| [`zstring name = sampGetCurrentServerName()`](lua/sampGetCurrentServerName.md) |
| [`sampShowDialog(int id, zstring caption, zstring text, zstring button1, zstring button2, int style)`](lua/sampShowDialog.md) |
| [`bool result, int button, int list, zstring input = sampHasDialogRespond(int id)`](lua/sampHasDialogRespond.md) |
| [`Bitstream bs = raknetNewBitStream()`](lua/raknetNewBitStream.md) |
| [`raknetDeleteBitStream(Bitstream bs)`](lua/raknetDeleteBitStream.md) |
| [`raknetResetBitStream(Bitstream bs)`](lua/raknetResetBitStream.md) |
| [`raknetBitStreamWriteBool(Bitstream bs, bool value)`](lua/raknetBitStreamWriteBool.md) |
| [`raknetBitStreamWriteInt8(Bitstream bs, int value)`](lua/raknetBitStreamWriteInt8.md) |
| [`raknetBitStreamWriteInt16(Bitstream bs, int value)`](lua/raknetBitStreamWriteInt16.md) |
| [`raknetBitStreamWriteInt32(Bitstream bs, int value)`](lua/raknetBitStreamWriteInt32.md) |
| [`raknetBitStreamWriteFloat(Bitstream bs, float value)`](lua/raknetBitStreamWriteFloat.md) |
| [`raknetBitStreamWriteBuffer(Bitstream bs, uint dest, uint size)`](lua/raknetBitStreamWriteBuffer.md) |
| [`raknetBitStreamWriteBitStream(Bitstream bs, Bitstream bitStream)`](lua/raknetBitStreamWriteBitStream.md) |
| [`raknetBitStreamWriteString(Bitstream bs, string str)`](lua/raknetBitStreamWriteString.md) |
| [`raknetSendRpcEx(int rpc, Bitstream bs, int priority, int reliability, int channel, bool timestamp)`](lua/raknetSendRpcEx.md) |
| [`raknetSendBitStreamEx(Bitstream bs, int priority, int reliability, int channel)`](lua/raknetSendBitStreamEx.md) |
| [`int textlabel = sampCreate3dText(zstring text, uint color, float posX, float posY, float posZ, float distance, bool ignoreWalls, int playerId, int vehicleId)`](lua/sampCreate3dText.md) |
| [`sampDestroy3dText(int textlabel)`](lua/sampDestroy3dText.md) |
| [`bool result = sampIs3dTextDefined(int 3dText)`](lua/sampIs3dTextDefined.md) |
| [`sampCloseCurrentDialogWithButton(int button)`](lua/sampCloseCurrentDialogWithButton.md) |
| [`int list = sampGetCurrentDialogListItem()`](lua/sampGetCurrentDialogListItem.md) |
| [`sampSetCurrentDialogListItem(int list)`](lua/sampSetCurrentDialogListItem.md) |
| [`zstring text = sampGetCurrentDialogEditboxText()`](lua/sampGetCurrentDialogEditboxText.md) |
| [`sampSetCurrentDialogEditboxText(zstring text)`](lua/sampSetCurrentDialogEditboxText.md) |
| [`bool result = sampIsDialogActive()`](lua/sampIsDialogActive.md) |
| [`int type = sampGetCurrentDialogType()`](lua/sampGetCurrentDialogType.md) |
| [`int id = sampGetCurrentDialogId()`](lua/sampGetCurrentDialogId.md) |
| [`int gamestate = sampGetGamestate()`](lua/sampGetGamestate.md) |
| [`Object object = sampGetObjectHandleBySampId(int id)`](lua/sampGetObjectHandleBySampId.md) |
| [`Pickup pickup = sampGetPickupHandleBySampId(int id)`](lua/sampGetPickupHandleBySampId.md) |
| [`int objectId = sampGetObjectSampIdByHandle(Object object)`](lua/sampGetObjectSampIdByHandle.md) |
| [`int pickupId = sampGetPickupSampIdByHandle(Pickup pickup)`](lua/sampGetPickupSampIdByHandle.md) |
| [`int count = sampGetListboxItemsCount()`](lua/sampGetListboxItemsCount.md) |
| [`int animid = sampGetPlayerAnimationId(int playerId)`](lua/sampGetPlayerAnimationId.md) |
| [`zstring file, zstring name = sampGetAnimationNameAndFile(int animid)`](lua/sampGetAnimationNameAndFile.md) |
| [`int id = sampFindAnimationIdByNameAndFile(zstring name, zstring file)`](lua/sampFindAnimationIdByNameAndFile.md) |
| [`int resX, int resY = getScreenResolution()`](lua/getScreenResolution.md) |
| [`zstring text = sampGetListboxItemText(int item)`](lua/sampGetListboxItemText.md) |
| [`bool result = sampIsPlayerPaused(int id)`](lua/sampIsPlayerPaused.md) |
| [`sampToggleCursor(bool show)`](lua/sampToggleCursor.md) |
| [`bool result = sampIsLocalPlayerSpawned()`](lua/sampIsLocalPlayerSpawned.md) |
| [`int action = sampGetPlayerSpecialAction(int id)`](lua/sampGetPlayerSpecialAction.md) |
| [`bool result = sampUnregisterChatCommand(zstring cmd)`](lua/sampUnregisterChatCommand.md) |
| [`bool result = sampIsPlayerNpc(int id)`](lua/sampIsPlayerNpc.md) |
| [`int score = sampGetPlayerScore(int id)`](lua/sampGetPlayerScore.md) |
| [`sampSetChatString(int id, zstring text, zstring prefix, uint color, uint pcolor)`](lua/sampSetChatString.md) |
| [`zstring text, zstring prefix, uint color, uint pcolor = sampGetChatString(int id)`](lua/sampGetChatString.md) |
| [`sampSetChatInputText(zstring text)`](lua/sampSetChatInputText.md) |
| [`zstring text = sampGetChatInputText()`](lua/sampGetChatInputText.md) |
| [`sampfuncsLog(zstring msg)`](lua/sampfuncsLog.md) |
| [`sampSetChatInputEnabled(bool enabled)`](lua/sampSetChatInputEnabled.md) |
| [`uint rakclientPtr = sampGetRakclientInterface()`](lua/sampGetRakclientInterface.md) |
| [`uint rakpeer = sampGetRakpeer()`](lua/sampGetRakpeer.md) |
| [`uint address = sampGetRakclientFuncAddressByIndex(int index)`](lua/sampGetRakclientFuncAddressByIndex.md) |
| [`uint callbackAddress = sampGetRpcCallbackByRpcId(int index)`](lua/sampGetRpcCallbackByRpcId.md) |
| [`uint node = sampGetRpcNodeByRpcId(int index)`](lua/sampGetRpcNodeByRpcId.md) |
| [`uint sampPtr = sampGetSampInfoPtr()`](lua/sampGetSampInfoPtr.md) |
| [`DxutDialog dialog = dxutCreateDialog(zstring name)`](lua/dxutCreateDialog.md) |
| [`bool result, int event, int id = dxutPopEvent(DxutDialog dialog)`](lua/dxutPopEvent.md) |
| [`dxutAddButton(DxutDialog dialog, int id, zstring text, int posX, int posY, int sizeX, int sizeY)`](lua/dxutAddButton.md) |
| [`dxutAddCheckbox(DxutDialog dialog, int id, zstring text, int posX, int posY, int sizeX, int sizeY)`](lua/dxutAddCheckbox.md) |
| [`dxutSetDialogPos(DxutDialog dialog, int posX, int posY, int sizeX, int sizeY)`](lua/dxutSetDialogPos.md) |
| [`int posX, int posY, int sizeX, int sizeY = dxutGetDialogPosAndSize(DxutDialog dialog)`](lua/dxutGetDialogPosAndSize.md) |
| [`dxutSetDialogVisible(DxutDialog dialog, bool visible)`](lua/dxutSetDialogVisible.md) |
| [`bool result = dxutIsDialogVisible(DxutDialog dialog)`](lua/dxutIsDialogVisible.md) |
| [`dxutAddEditbox(DxutDialog dialog, int id, zstring text, int posX, int posY, int sizeX, int sizeY)`](lua/dxutAddEditbox.md) |
| [`zstring text = dxutGetControlText(DxutDialog dialog, int id)`](lua/dxutGetControlText.md) |
| [`raknetSendRpc(int rpc, Bitstream bs)`](lua/raknetSendRpc.md) |
| [`raknetSendBitStream(Bitstream bs)`](lua/raknetSendBitStream.md) |
| [`bool result = sampIsCursorActive()`](lua/sampIsCursorActive.md) |
| [`sampSetCursorMode(int mode)`](lua/sampSetCursorMode.md) |
| [`int mode = sampGetCursorMode()`](lua/sampGetCursorMode.md) |
| [`dxutSetControlVisible(DxutDialog dialog, int id, bool visible)`](lua/dxutSetControlVisible.md) |
| [`dxutAddStatic(DxutDialog dialog, int id, zstring text, int posX, int posY, int sizeX, int sizeY)`](lua/dxutAddStatic.md) |
| [`bool result = dxutIsCheckboxChecked(DxutDialog dialog, int id)`](lua/dxutIsCheckboxChecked.md) |
| [`dxutSetDialogBackgroundColor(DxutDialog dialog, uint color)`](lua/dxutSetDialogBackgroundColor.md) |
| [`dxutSetControlText(DxutDialog dialog, int id, zstring text)`](lua/dxutSetControlText.md) |
| [`bool result = dxutControlIsVisible(DxutDialog dialog, int id)`](lua/dxutControlIsVisible.md) |
| [`dxutAddSlider(DxutDialog dialog, int id, int posX, int posY, int sizeX, int sizeY, int max)`](lua/dxutAddSlider.md) |
| [`int value = dxutGetSliderValue(DxutDialog dialog, int id)`](lua/dxutGetSliderValue.md) |
| [`dxutSetSliderValue(DxutDialog dialog, int id, int value)`](lua/dxutSetSliderValue.md) |
| [`dxutAddListbox(DxutDialog dialog, int id, int posX, int posY, int sizeX, int sizeY)`](lua/dxutAddListbox.md) |
| [`dxutListboxInsertItem(DxutDialog dialog, int id, zstring element, uint data, int after)`](lua/dxutListboxInsertItem.md) |
| [`int element, int count = dxutGetListboxSelectedItemAndCount(DxutDialog dialog, int id)`](lua/dxutGetListboxSelectedItemAndCount.md) |
| [`dxutListboxDeleteItem(DxutDialog dialog, int id, int element)`](lua/dxutListboxDeleteItem.md) |
| [`zstring text, uint data = dxutGetListboxItemTextAndData(DxutDialog dialog, int id, int element)`](lua/dxutGetListboxItemTextAndData.md) |
| [`dxutCheckboxSetChecked(DxutDialog dialog, int id, bool checked)`](lua/dxutCheckboxSetChecked.md) |
| [`dxutEnableDialogCaption(DxutDialog dialog, bool enable)`](lua/dxutEnableDialogCaption.md) |
| [`bool result = dxutIsDialogCaptionEnabled(DxutDialog dialog)`](lua/dxutIsDialogCaptionEnabled.md) |
| [`dxutSetDialogMinimized(DxutDialog dialog, bool minimized)`](lua/dxutSetDialogMinimized.md) |
| [`bool result = dxutIsDialogMinimized(DxutDialog dialog)`](lua/dxutIsDialogMinimized.md) |
| [`dxutDeleteControl(DxutDialog dialog, int id)`](lua/dxutDeleteControl.md) |
| [`dxutDeleteDialog(DxutDialog dialog)`](lua/dxutDeleteDialog.md) |
| [`dxutSetFocusOnControl(DxutDialog dialog, int id)`](lua/dxutSetFocusOnControl.md) |
| [`dxutSetControlSize(DxutDialog dialog, int id, int sizeX, int sizeY)`](lua/dxutSetControlSize.md) |
| [`int sizeX, int sizeY = dxutGetControlSize(DxutDialog dialog, int id)`](lua/dxutGetControlSize.md) |
| [`dxutSetControlPos(DxutDialog dialog, int id, int posX, int posY)`](lua/dxutSetControlPos.md) |
| [`int posX, int posY = dxutGetControlPos(DxutDialog dialog, int id)`](lua/dxutGetControlPos.md) |
| [`dxutSetCheckboxColor(DxutDialog dialog, int id, uint color)`](lua/dxutSetCheckboxColor.md) |
| [`bool result = dxutIsDialogExists(DxutDialog dialog)`](lua/dxutIsDialogExists.md) |
| [`uint settingsPtr = sampGetServerSettingsPtr()`](lua/sampGetServerSettingsPtr.md) |
| [`uint poolsPtr = sampGetSampPoolsPtr()`](lua/sampGetSampPoolsPtr.md) |
| [`uint chatPtr = sampGetChatInfoPtr()`](lua/sampGetChatInfoPtr.md) |
| [`uint inputPtr = sampGetInputInfoPtr()`](lua/sampGetInputInfoPtr.md) |
| [`uint dialogPtr = sampGetDialogInfoPtr()`](lua/sampGetDialogInfoPtr.md) |
| [`uint kill = sampGetKillInfoPtr()`](lua/sampGetKillInfoPtr.md) |
| [`uint miscPtr = sampGetMiscInfoPtr()`](lua/sampGetMiscInfoPtr.md) |
| [`uint tdpoolPtr = sampGetTextdrawPoolPtr()`](lua/sampGetTextdrawPoolPtr.md) |
| [`int objpoolPtr = sampGetObjectPoolPtr()`](lua/sampGetObjectPoolPtr.md) |
| [`uint gzpoolPtr = sampGetGangzonePoolPtr()`](lua/sampGetGangzonePoolPtr.md) |
| [`uint tlabelpoolPtr = sampGetTextlabelPoolPtr()`](lua/sampGetTextlabelPoolPtr.md) |
| [`uint playerpoolPtr = sampGetPlayerPoolPtr()`](lua/sampGetPlayerPoolPtr.md) |
| [`uint vehpoolPtr = sampGetVehiclePoolPtr()`](lua/sampGetVehiclePoolPtr.md) |
| [`uint pickuppoolPtr = sampGetPickupPoolPtr()`](lua/sampGetPickupPoolPtr.md) |
| [`sampStorePlayerOnfootData(int id, uint dstBuffer)`](lua/sampStorePlayerOnfootData.md) |
| [`sampStorePlayerIncarData(int id, uint dstBuffer)`](lua/sampStorePlayerIncarData.md) |
| [`sampStorePlayerPassengerData(int id, uint dstBuffer)`](lua/sampStorePlayerPassengerData.md) |
| [`sampStorePlayerTrailerData(int id, uint dstBuffer)`](lua/sampStorePlayerTrailerData.md) |
| [`sampStorePlayerAimData(int id, uint dstBuffer)`](lua/sampStorePlayerAimData.md) |
| [`sampSendRconCommand(zstring cmd)`](lua/sampSendRconCommand.md) |
| [`sampSendOnfootData(uint dataPtr)`](lua/sampSendOnfootData.md) |
| [`sampSendIncarData(uint dataPtr)`](lua/sampSendIncarData.md) |
| [`sampSendPassengerData(uint dataPtr)`](lua/sampSendPassengerData.md) |
| [`sampSendAimData(uint dataPtr)`](lua/sampSendAimData.md) |
| [`sampSendBulletData(uint dataPtr)`](lua/sampSendBulletData.md) |
| [`sampSendTrailerData(uint dataPtr)`](lua/sampSendTrailerData.md) |
| [`sampSendUnoccupiedData(uint dataPtr)`](lua/sampSendUnoccupiedData.md) |
| [`sampSendSpectatorData(uint dataPtr)`](lua/sampSendSpectatorData.md) |
| [`sampSendClickPlayer(int id, int source)`](lua/sampSendClickPlayer.md) |
| [`sampSendDialogResponse(int id, int button, int listitem, zstring input)`](lua/sampSendDialogResponse.md) |
| [`sampSendClickTextdraw(int id)`](lua/sampSendClickTextdraw.md) |
| [`sampSendGiveDamage(int id, float damage, int weapon, int bodypart)`](lua/sampSendGiveDamage.md) |
| [`sampSendTakeDamage(int id, float damage, int weapon, int bodypart)`](lua/sampSendTakeDamage.md) |
| [`sampSendEditObject(bool playerObject, int objectId, int response, float posX, float posY, float posZ, float rotX, float rotY, float rotZ)`](lua/sampSendEditObject.md) |
| [`sampSendEditAttachedObject(int response, int index, int model, int bone, float offsetX, float offsetY, float offsetZ, float rotX, float rotY, float rotZ, float scaleX, float scaleY, float scaleZ)`](lua/sampSendEditAttachedObject.md) |
| [`sampSendInteriorChange(int id)`](lua/sampSendInteriorChange.md) |
| [`sampSendRequestSpawn()`](lua/sampSendRequestSpawn.md) |
| [`sampSendPickedUpPickup(int id)`](lua/sampSendPickedUpPickup.md) |
| [`sampSendMenuSelectRow(int id)`](lua/sampSendMenuSelectRow.md) |
| [`sampSendMenuQuit()`](lua/sampSendMenuQuit.md) |
| [`sampSendVehicleDestroyed(int id)`](lua/sampSendVehicleDestroyed.md) |
| [`bool result = sampIsScoreboardOpen()`](lua/sampIsScoreboardOpen.md) |
| [`sampToggleScoreboard(bool show)`](lua/sampToggleScoreboard.md) |
| [`zstring text = sampGetDialogText()`](lua/sampGetDialogText.md) |
| [`zstring caption = sampGetDialogCaption()`](lua/sampGetDialogCaption.md) |
| [`sampSetDialogClientside(bool clientside)`](lua/sampSetDialogClientside.md) |
| [`bool result = sampIsDialogClientside()`](lua/sampIsDialogClientside.md) |
| [`bool result = sampIsChatVisible()`](lua/sampIsChatVisible.md) |
| [`int mode = sampGetChatDisplayMode()`](lua/sampGetChatDisplayMode.md) |
| [`sampSetChatDisplayMode(int mode)`](lua/sampSetChatDisplayMode.md) |
| [`pauseScmThread(uint thread)`](lua/pauseScmThread.md) |
| [`resumeScmThread(uint thread)`](lua/resumeScmThread.md) |
| [`bool value = raknetBitStreamReadBool(Bitstream bs)`](lua/raknetBitStreamReadBool.md) |
| [`int value = raknetBitStreamReadInt8(Bitstream bs)`](lua/raknetBitStreamReadInt8.md) |
| [`int value = raknetBitStreamReadInt16(Bitstream bs)`](lua/raknetBitStreamReadInt16.md) |
| [`int value = raknetBitStreamReadInt32(Bitstream bs)`](lua/raknetBitStreamReadInt32.md) |
| [`float value = raknetBitStreamReadFloat(Bitstream bs)`](lua/raknetBitStreamReadFloat.md) |
| [`raknetBitStreamReadBuffer(Bitstream bs, uint dest, uint size)`](lua/raknetBitStreamReadBuffer.md) |
| [`string value = raknetBitStreamReadString(Bitstream bs, uint size)`](lua/raknetBitStreamReadString.md) |
| [`raknetBitStreamResetReadPointer(Bitstream bs)`](lua/raknetBitStreamResetReadPointer.md) |
| [`raknetBitStreamResetWritePointer(Bitstream bs)`](lua/raknetBitStreamResetWritePointer.md) |
| [`raknetBitStreamIgnoreBits(Bitstream bs, int amount)`](lua/raknetBitStreamIgnoreBits.md) |
| [`raknetBitStreamSetWriteOffset(Bitstream bs, int offset)`](lua/raknetBitStreamSetWriteOffset.md) |
| [`raknetBitStreamSetReadOffset(Bitstream bs, int offset)`](lua/raknetBitStreamSetReadOffset.md) |
| [`uint value = raknetBitStreamGetNumberOfBitsUsed(Bitstream bs)`](lua/raknetBitStreamGetNumberOfBitsUsed.md) |
| [`uint value = raknetBitStreamGetNumberOfBytesUsed(Bitstream bs)`](lua/raknetBitStreamGetNumberOfBytesUsed.md) |
| [`uint value = raknetBitStreamGetNumberOfUnreadBits(Bitstream bs)`](lua/raknetBitStreamGetNumberOfUnreadBits.md) |
| [`int value = raknetBitStreamGetWriteOffset(Bitstream bs)`](lua/raknetBitStreamGetWriteOffset.md) |
| [`int value = raknetBitStreamGetReadOffset(Bitstream bs)`](lua/raknetBitStreamGetReadOffset.md) |
| [`uint value = raknetBitStreamGetDataPtr(Bitstream bs)`](lua/raknetBitStreamGetDataPtr.md) |
| [`zstring string = raknetBitStreamDecodeString(Bitstream bs, int size)`](lua/raknetBitStreamDecodeString.md) |
| [`raknetBitStreamEncodeString(Bitstream bs, zstring string)`](lua/raknetBitStreamEncodeString.md) |
| [`raknetEmulRpcReceiveBitStream(int rpc, Bitstream bs)`](lua/raknetEmulRpcReceiveBitStream.md) |
| [`raknetEmulPacketReceiveBitStream(int packet, Bitstream bs)`](lua/raknetEmulPacketReceiveBitStream.md) |
| [`zstring name = raknetGetRpcName(int rpc)`](lua/raknetGetRpcName.md) |
| [`zstring name = raknetGetPacketName(int packet)`](lua/raknetGetPacketName.md) |
| [`bool result = setSampfuncsGlobalVar(zstring var, int value)`](lua/setSampfuncsGlobalVar.md) |
| [`bool result, int value = getSampfuncsGlobalVar(zstring var)`](lua/getSampfuncsGlobalVar.md) |
| [`sampCreate3dTextEx(int id, zstring text, uint color, float posX, float posY, float posZ, float distance, bool ignoreWalls, int playerId, int vehicleId)`](lua/sampCreate3dTextEx.md) |
| [`zstring string, uint color, float posX, float posY, float posZ, float distance, bool ignoreWalls, int playerId, int vehicleId = sampGet3dTextInfoById(int id)`](lua/sampGet3dTextInfoById.md) |
| [`sampSet3dTextString(int id, zstring text)`](lua/sampSet3dTextString.md) |
| [`sampTextdrawCreate(int id, zstring text, float posX, float posY)`](lua/sampTextdrawCreate.md) |
| [`sampTextdrawSetBoxColorAndSize(int id, int box, uint color, float sizeX, float sizeY)`](lua/sampTextdrawSetBoxColorAndSize.md) |
| [`sampTextdrawSetAlign(int id, int align)`](lua/sampTextdrawSetAlign.md) |
| [`sampTextdrawSetProportional(int id, int proportional)`](lua/sampTextdrawSetProportional.md) |
| [`sampTextdrawSetStyle(int id, int style)`](lua/sampTextdrawSetStyle.md) |
| [`sampTextdrawSetShadow(int id, int shadow, uint color)`](lua/sampTextdrawSetShadow.md) |
| [`sampTextdrawSetOutlineColor(int id, int outline, uint color)`](lua/sampTextdrawSetOutlineColor.md) |
| [`sampTextdrawSetModelRotationZoomVehColor(int id, int model, float rotX, float rotY, float rotZ, float zoom, int clr1, int clr2)`](lua/sampTextdrawSetModelRotationZoomVehColor.md) |
| [`sampTextdrawSetString(int id, zstring text)`](lua/sampTextdrawSetString.md) |
| [`sampTextdrawSetPos(int id, float posX, float posY)`](lua/sampTextdrawSetPos.md) |
| [`sampTextdrawSetLetterSizeAndColor(int id, float letSizeX, float letSizeY, uint color)`](lua/sampTextdrawSetLetterSizeAndColor.md) |
| [`int box, uint color, float sizeX, float sizeY = sampTextdrawGetBoxEnabledColorAndSize(int id)`](lua/sampTextdrawGetBoxEnabledColorAndSize.md) |
| [`int align = sampTextdrawGetAlign(int id)`](lua/sampTextdrawGetAlign.md) |
| [`int prop = sampTextdrawGetProportional(int id)`](lua/sampTextdrawGetProportional.md) |
| [`int style = sampTextdrawGetStyle(int id)`](lua/sampTextdrawGetStyle.md) |
| [`int shadow, uint color = sampTextdrawGetShadowColor(int id)`](lua/sampTextdrawGetShadowColor.md) |
| [`int outline, uint color = sampTextdrawGetOutlineColor(int id)`](lua/sampTextdrawGetOutlineColor.md) |
| [`int model, float rotX, float rotY, float rotZ, float zoom, int clr1, int clr2 = sampTextdrawGetModelRotationZoomVehColor(int id)`](lua/sampTextdrawGetModelRotationZoomVehColor.md) |
| [`zstring text = sampTextdrawGetString(int id)`](lua/sampTextdrawGetString.md) |
| [`float posX, float posY = sampTextdrawGetPos(int id)`](lua/sampTextdrawGetPos.md) |
| [`float letSizeX, float letSizeY, uint color = sampTextdrawGetLetterSizeAndColor(int id)`](lua/sampTextdrawGetLetterSizeAndColor.md) |
| [`bool result = sampTextdrawIsExists(int id)`](lua/sampTextdrawIsExists.md) |
| [`sampTextdrawDelete(int id)`](lua/sampTextdrawDelete.md) |
| [`bool result = isSampfuncsGlobalVarDefined(zstring var)`](lua/isSampfuncsGlobalVarDefined.md) |
| [`bool read, bool write = getSampfuncsGlobalVarAccessForThread(zstring var, uint thread)`](lua/getSampfuncsGlobalVarAccessForThread.md) |
| [`runSampfuncsConsoleCommand(zstring cmd)`](lua/runSampfuncsConsoleCommand.md) |
| [`bool result = sampfuncsRegisterConsoleCommand(zstring cmd, function func)`](lua/sampfuncsRegisterConsoleCommand.md) |
| [`bool result = sampfuncsUnregisterConsoleCommand(zstring cmd)`](lua/sampfuncsUnregisterConsoleCommand.md) |
| [`uint thread = createScmThreadAtPointer(uint pointer, table args)`](lua/createScmThreadAtPointer.md) |
| [`setScmThreadLocalVar(uint thread, int var, any value)`](lua/setScmThreadLocalVar.md) |
| [`int value = getScmThreadLocalVar(uint thread, int var)`](lua/getScmThreadLocalVar.md) |
| [`destroyScmThread(uint thread)`](lua/destroyScmThread.md) |
| [`restartScmThread(uint thread, table args)`](lua/restartScmThread.md) |
| [`bool result = isSampfuncsConsoleActive()`](lua/isSampfuncsConsoleActive.md) |
| [`sampSetClientCommandDescription(zstring cmd, zstring text)`](lua/sampSetClientCommandDescription.md) |
| [`setSampfuncsConsoleCommandDescription(zstring cmd, zstring text)`](lua/setSampfuncsConsoleCommandDescription.md) |
| [`sampForceVehicleSync(int id)`](lua/sampForceVehicleSync.md) |
| [`sampForceUnoccupiedSyncSeatId(int id, int seatId)`](lua/sampForceUnoccupiedSyncSeatId.md) |
| [`sampForceOnfootSync()`](lua/sampForceOnfootSync.md) |
| [`sampForceAimSync()`](lua/sampForceAimSync.md) |
| [`sampForceTrailerSync(int id)`](lua/sampForceTrailerSync.md) |
| [`sampForcePassengerSyncSeatId(int id, int seatId)`](lua/sampForcePassengerSyncSeatId.md) |
| [`sampForceStatsSync()`](lua/sampForceStatsSync.md) |
| [`sampForceWeaponsSync()`](lua/sampForceWeaponsSync.md) |
| [`int id = sampGetMaxPlayerId(bool streamed)`](lua/sampGetMaxPlayerId.md) |
| [`int count = sampGetPlayerCount(bool streamed)`](lua/sampGetPlayerCount.md) |
| [`sampProcessChatInput(zstring text)`](lua/sampProcessChatInput.md) |
| [`bool result = sampIsChatCommandDefined(zstring cmd)`](lua/sampIsChatCommandDefined.md) |
| [`bool result = isSampfuncsConsoleCommandDefined(zstring cmd)`](lua/isSampfuncsConsoleCommandDefined.md) |
| [`int version = getCleoLibraryVersion()`](lua/getCleoLibraryVersion.md) |
| [`main()`](lua/main.md) |
| [`onExitScript(bool quitGame)`](lua/onExitScript.md) |
| [`onQuitGame()`](lua/onQuitGame.md) |
| [`onScriptLoad(LuaScript s)`](lua/onScriptLoad.md) |
| [`onScriptTerminate(LuaScript s, bool quitGame)`](lua/onScriptTerminate.md) |
| [`onSystemInitialized()`](lua/onSystemInitialized.md) |
| [`onScriptMessage(string msg, LuaScript s)`](lua/onScriptMessage.md) |
| [`onSystemMessage(string msg, int type, LuaScript s)`](lua/onSystemMessage.md) |
| [`bool process=true, int id, bitstream bitStream = onReceivePacket(int id, bitstream bitStream)`](lua/onReceivePacket.md) |
| [`bool process=true, int id, bitstream bitStream = onReceiveRpc(int id, bitstream bitStream)`](lua/onReceiveRpc.md) |
| [`bool process=true, int id, bitstream bitStream, int priority, int reliability, int orderingChannel = onSendPacket(int id, bitstream bitStream, int priority, int reliability, int orderingChannel)`](lua/onSendPacket.md) |
| [`bool process=true, int id, bitstream bitStream, int priority, int reliability, int orderingChannel, bool shiftTs = onSendRpc(int id, bitstream bitStream, int priority, int reliability, int orderingChannel, bool shiftTs)`](lua/onSendRpc.md) |
| [`onWindowMessage(uint msg, uint wparam, int lparam)`](lua/onWindowMessage.md) |
| [`onStartNewGame(int mpack)`](lua/onStartNewGame.md) |
| [`onLoadGame(table saveData)`](lua/onLoadGame.md) |
| [`table newSaveData = onSaveGame(table saveData)`](lua/onSaveGame.md) |
| [`Ped PLAYER_PED`](lua/PLAYER_PED.md) |
| [`Player PLAYER_HANDLE`](lua/PLAYER_HANDLE.md) |
| [`Ped playerPed`](lua/playerPed.md) |
| [`Player playerHandle`](lua/playerHandle.md) |
