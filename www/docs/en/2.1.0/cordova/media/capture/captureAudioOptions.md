---
license: >
    Licensed to the Apache Software Foundation (ASF) under one
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

title: CaptureAudioOptions
---

CaptureAudioOptions
===================

> Encapsulates audio capture configuration options.

Properties
----------

- __limit:__ The maximum number of audio clips the device user can record in a single capture operation.  The value must be greater than or equal to 1 (defaults to 1).
- __duration:__ The maximum duration of an audio sound clip, in seconds.
- __mode:__ The selected audio mode.  The value must match one of the elements in `capture.supportedAudioModes`.

Quick Example
-------------

    // limit capture operation to 3 media files, no longer than 10 seconds each
    var options = { limit: 3, duration: 10 };

    navigator.device.capture.captureAudio(captureSuccess, captureError, options);

Android Quirks
--------------

- The __duration__ parameter is not supported.  Recording lengths cannot be limited programmatically.
- The __mode__ parameter is not supported.  The audio recording format cannot be altered programmatically.  Recordings are encoded using Adaptive Multi-Rate (AMR) format (audio/amr).

BlackBerry WebWorks Quirks
--------------------------

- The __duration__ parameter is not supported.  Recording lengths cannot be limited programmatically.
- The __mode__ parameter is not supported.  The audio recording format cannot be altered programmatically.  Recordings are encoded using Adaptive Multi-Rate (AMR) format (audio/amr).

iOS Quirks
----------

- The __limit__ parameter is not supported. One recording can be created for each invocation.
- The __mode__ parameter is not supported.  The audio recording format cannot be altered programmatically.  Recordings are encoded using Waveform Audio (WAV) format (audio/wav).