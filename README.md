![version](https://img.shields.io/badge/version-1.1.0-green.svg?style=flat-square)
![badge](https://img.shields.io/badge/for-instagram-yellow.svg?style=flat-square)

# [instantgram]

[instantgram] is a bookmarklet with purpose of download instagram images. Tiny, simple, without necessity of extensions or downloads. Just drag the [instantgram] link below to bookmark bar of your browser, navigate to the instagram.com (web), open a instagram post (photo) and click at bookmarklet. Just works.

## [[instantgram]][1]

## Roadmap

- a way of notify updates in [instantgram]

[1]:javascript:(function()%7B%22use%20strict%22%3Bvar%20VERSION%3D%221.1.0%22%2Chostname%3Dlocation.hostname%2Cpath%3Dlocation.pathname%2Chref%3Dlocation.href%2Cimages%3Ddocument.images%2Cregex_original_image%3D%2F%5C%2F%5Ba-z%5D%2B%5Cd%2B%5Ba-z%5D%3Fx%5Cd%2B%5Ba-z%5D%3F%2F%2Cregex_path%3D%2F%5E%5C%2Fp%5C%2F%2F%2Cregex_hostname%3D%2Finstagram%5C.com%2F%3Bif(regex_hostname.test(hostname)%7C%7Calert(%22%5Binstantgram%5D%20only%20works%20in%20instagram.com%22)%2Cregex_hostname.test(hostname))if(regex_path.test(path))%7Btry%7Bif(2%3D%3D%3Ddocument.getElementsByTagName(%22article%22).length)%7Bvar%20modal%3Ddocument.getElementsByTagName(%22article%22)%5B1%5D%2Cmodal_image%3Dmodal.children%5B1%5D.firstChild.firstChild.firstChild.src%3Bif(modal_image)%7Bvar%20image_link%3Dregex_original_image.test(modal_image)%3Fmodal_image.replace(regex_original_image%2C%22%22)%3Amodal_image%3Bwindow.open(modal_image)%7Delse%20alert(%22%5Binstantgram%5D%20don't%20found%20a%20image%20in%20instagram%20post.%20Try%20open%20the%20link%20in%20new%20tab.%22)%7D%7Dcatch(e)%7Bconsole.error(%22%5Binstantgram%5D%20%22%2BVERSION%2Ce)%7Dtry%7Bif(1%3D%3D%3Ddocument.getElementsByTagName(%22article%22).length)%7Bvar%20post%3Ddocument.getElementsByTagName(%22article%22)%5B0%5D%2Cpost_image%3Dpost.children%5B1%5D.firstChild.firstChild.firstChild.src%2Cimage_link%3Dregex_original_image.test(post_image)%3Fpost_image.replace(regex_original_image%2C%22%22)%3Apost_image%3Bwindow.open(image_link)%7Delse%20alert(%22ops%2C%20%5Binstantgram%5D%20don't%20found%20the%20image%20%3A(%22)%7Dcatch(e)%7Bconsole.error(%22%5Binstantgram%5D%20%22%2BVERSION%2Ce)%7D%7Delse%20alert(%22ops%2C%20are%20you%20in%20a%20instagram%20post%3F%20ex%3A%20instagram.com%2Fp%2F82jd828jd%22)%3B%7D)()
