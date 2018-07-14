# Como-convertir-un-objeto-a-JSON-y-Guardarlos-con-SharedPreferences-Android

## Guardar

```
SharedPreferences  mPrefs = getPreferences("Key",MODE_PRIVATE);

- To save:

Editor prefsEditor = mPrefs.edit();
Gson gson = new Gson();
String json = gson.toJson(MyObject);
prefsEditor.putString("MyObject", json);
prefsEditor.commit();

- To retrieve:

Gson gson = new Gson();
String json = mPrefs.getString("MyObject", "");
MyObject obj = gson.fromJson(json, MyObject.class);

```
