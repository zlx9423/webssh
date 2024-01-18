learning coding

需要自己输入的部分是:build and development setting 下  Run command
huashengdun/webssh

python run.py --xsrf=False --xheaders=False --origin='*' --debug --delay=6


以及 Exposing your service   Port:8888

workers反代代码


export default {
  async fetch(request, env) {
    let url = new URL(request.url);
    if (url.pathname.startsWith('/')) {
      url.hostname = 'flexible-kaylee-kj123.koyeb.app' //自定义域//
      let new_request = new Request(url, request);
      return fetch(new_request);
    }
    return env.ASSETS.fetch(request);
  },
};


url.hostname = ssh.website2024.dedyn.io


//https://zelikk.blogspot.com/2023/10/huashengdun-webssh-codesandbox.html
//https://github.com/huashengdun/webssh//
