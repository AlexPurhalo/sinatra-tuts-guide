<h2>Progress</h2>
<ul>
    <li><h5>$ ruby application.rb</h5></li>
    <li>
        <h5>$ curl http://localhost:4567</h5>
        <p>output: "<strong>Hello World!</strong>" in console</p>
    </li>
    <li><h5>$ ruby -Ilib application.rb</h5></li>
    <li>
        <h5>$ curl http://localhost:4567/reviews</h5>
        <p>output: empty array <strong>[]</strong></p>
    </li>
    <li>
        <h5>$ curl -d "review[name]=Hello&review[text]=World" http://localhost:4567/reviews</h5>
        <p>$ curl http://localhost:4567/reviews</p>
        <p>output: <strong>[</strong>{"id":1,"name":"Hello","text":"World","created_at":"2016-09-29T09:28:20-04:00","updated_at":"2016-09-29T09:28:20-04:00"}<strong>]</strong></p>
    </li>
    <li>
        <h5><strong>$ curl http://localhost:4567/reviews/1</strong></h5>
        <p>output: <strong>{<strong/>"id":1,"name":"Hello","text":"World","created_at":"2016-09-29T09:28:20-04:00","updated_at":"2016-09-29T09:28:20-04:00"<strong>}</strong></p>
    </li>
    <li>
        <h5>$curl -X PUT -d "review[name]=Goodbye" http://localhost:4567/reviews/1</h5>
        <p>output: "<strong>Review was updated</strong>"</p>
        <p>$ curl http://localhost:4567/reviews/1</p>
        <p>output: {"id":1,"name":"<strong>Goodbye</strong>","text":"World","created_at":"2016-09-29T09:28:20-04:00","updated_at":"2016-09-29T09:34:07-04:00"}</p>
    </li>
    <li>
        <h5><strong>$ curl -X DELETE  http://localhost:4567/reviews/1</strong></h5>
        <p>output: "<strong>Review was removed</strong>"</p>
        <p>$ curl http://localhost:4567/reviews</p>
        <p>output: empty object: <strong>[]</strong></p>
    </li>
</ul>