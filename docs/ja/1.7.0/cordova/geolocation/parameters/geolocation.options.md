---
license: Licensed to the Apache Software Foundation (ASF) under one
         or more contributor license agreements.  See the NOTICE file
         distributed with this work for additional information
         regarding copyright ownership.  The ASF licenses this file
         to you under the Apache License, Version 2.0 (the
         "License"); you may not use this file except in compliance
         with the License.  You may obtain a copy of the License at

           http://www.apache.org/licenses/LICENSE-2.0

         Unless required by applicable law or agreed to in writing,
         software distributed under the License is distributed on an
         "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
         KIND, either express or implied.  See the License for the
         specific language governing permissions and limitations
         under the License.
---

geolocationOptions
==================

位置情報取得の設定をカスタマイズするためのパラメーターを表します。

    { maximumAge: 3000, timeout: 5000, enableHighAccuracy: true };

オプション
-------

- __frequency:__ 位置情報を取得する頻度をミリ秒で表します。 このオプションは W3C の仕様に含まれておらず、将来的には実装が廃止されます。 maximumAge を代わりに使用してください。 _(Number)_ (デフォルト: 10000)
- __enableHighAccuracy:__ より精度の高い位置情報を取得するためのヒントを提供するかどうかを表します _(Boolean)_
- __timeout:__ `geolocation.getCurrentPosition` または `geolocation.watchPosition` 関数が呼び出されたときに、それぞれに対応する `geolocationSuccess` コールバック関数が呼ばれるまでの最大経過時間をミリ秒単位で表します _(Number)_
- __maximumAge:__ キャッシュされた位置情報の取得を許容する最大時間をミリ秒単位で表します _(Number)_

Android に関する注意点
--------------

Android 2.x のシミュレーターは enableHighAccuracy オプションが true にセットしない限り位置情報の取得結果を通知しません。

    { enableHighAccuracy: true }

