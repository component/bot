
# component-bot

  Component bot helping keep the component community badass.

## API

### Bot(user:String, pass:String)

  Initialize a new Bot with `user` / `pass`.

### Bot#issue(repo:String, title:String, body:String, [options]:Object)

  Create an issue with the given `title`, `body`, and `options`.
  
      bot
      .issue('visionmedia/superagent', 'Some issue', 'Check this out')
      .end(function(res){
        console.log(res.status);
        console.log(res.body);
      })

### Bot#commit(repo:String, msg:String, [fn]:Function)

  Commit to `repo` with the given `msg` and invoke `fn(err)`.
  
     bot.commit('visionmedia/superagent', 'add license property to component.json');

### Bot#clone(repo:String, fn:Function)

  Clone `repo` to the `/tmp` directory and invoke `fn(err, path)`.
  
     bot.clone('visionmedia/superagent', fn);

### Bot#fork(repo:String)

  Fork `repo`.

### Bot#pullrequest(repo:String, title:String, body:String)

  Send pull-request to `repo` with the given `title` and `body`.

## License 

  MIT
