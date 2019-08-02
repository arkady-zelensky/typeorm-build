There was a problem with MsSql driver - [tedious](https://github.com/tediousjs/tedious), when getting DB connection parameters from environment. There was [a type checking of number](https://github.com/tediousjs/tedious/blob/master/src/connection.js#L534), but port, passed from TypeORM was a stringy number, so it throws an error.

Solution: convert port to number.

to install:
`npm i arkady-zelensky/typeorm-build`

based on typeorm version 0.2.18

Done following [typeorm issue](https://github.com/typeorm/typeorm/issues/2271)
