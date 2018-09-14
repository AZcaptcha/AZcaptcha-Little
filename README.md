# [AZcaptcha.com] API
Little wrapper for AZcaptcha.com API

[![Build Status](https://travis-ci.org/AZcaptcha/AZcaptcha.com.svg?branch=master)](https://travis-ci.org/AZcaptcha/AZcaptcha.com)

## Go get

    go get github.com/AZcaptcha/AZcaptcha.com


## Upload image base64

    twocaptcha, _ := captcha.New("yourKey")
    captchaID, err := twocaptcha.UploadBase64Image("dHdvY2FwdGNoYQ==")

## Polling result

    iniAveragePollingTime := 1
    pollingTime := 1
    solution, err := twocaptcha.PollingCaptchaResponse(captchaID, iniAveragePollingTime, pollingTime)
    if err != nil {
	t.Errorf("unable to get captcha response: %s", err)
    }
