# Matter.Body

The`Matter.Body`module contains methods for creating and manipulating body models. A`Matter.Body`is a rigid body that can be simulated by a`Matter.Engine`. Factories for commonly used body configurations \(such as rectangles, circles and other polygons\) can be found in the module`Matter.Bodies`.

See the included usage[examples](https://github.com/liabru/matter-js/tree/master/examples).

* [Methods](http://brm.io/matter-js/docs/classes/Body.html#methods)
* [Properties](http://brm.io/matter-js/docs/classes/Body.html#properties)
* [Events](http://brm.io/matter-js/docs/classes/Body.html#events)

## Methods

### Matter.Body.[applyForce](http://brm.io/matter-js/docs/classes/Body.html#method_applyForce)

\(

body

,

position

,

force

\)



Applies a force to a body from a given world-space position, including resulting torque.

#### Parameters

* `body`
  [Body](http://brm.io/matter-js/docs/classes/Body.html)
* `position`
  [Vector](http://brm.io/matter-js/docs/classes/Vector.html)
* `force`
  [Vector](http://brm.io/matter-js/docs/classes/Vector.html)

@

[`src/body/Body.js:622`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l622)

### Matter.Body.[create](http://brm.io/matter-js/docs/classes/Body.html#method_create)

\(

options

\)

→

[Body](http://brm.io/matter-js/docs/classes/Body.html)



Creates a new rigid body model. The options parameter is an object that specifies any properties you wish to override the defaults. All properties have default values, and many are pre-calculated automatically based on other properties. Vertices must be specified in clockwise order. See the properties section below for detailed information on what you can pass via the`options`object.

#### Parameters

* `options`
  [Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)

#### Returns

[Body](http://brm.io/matter-js/docs/classes/Body.html)

body

@

[`src/body/Body.js:30`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l30)

### Matter.Body.[nextCategory](http://brm.io/matter-js/docs/classes/Body.html#method_nextCategory)

\(\)

→

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)



Returns the next unique category bitfield \(starting after the initial default category`0x0001`\). There are 32 available. See`body.collisionFilter`for more information.

#### Returns

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)

Unique category bitfield

@

[`src/body/Body.js:110`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l110)

### Matter.Body.[nextGroup](http://brm.io/matter-js/docs/classes/Body.html#method_nextGroup)

\(

\[isNonColliding=false\]

\)

→

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)



Returns the next unique group index for which bodies will collide. If`isNonColliding`is`true`, returns the next unique group index for which bodies will_not_collide. See`body.collisionFilter`for more information.

#### Parameters

* `[isNonColliding=false]`
  Bool
  optional

#### Returns

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)

Unique group index

@

[`src/body/Body.js:95`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l95)

### Matter.Body.[rotate](http://brm.io/matter-js/docs/classes/Body.html#method_rotate)

\(

body

,

rotation

,

\[point\]

\)



Rotates a body by a given angle relative to its current angle, without imparting any angular velocity.

#### Parameters

* `body`
  [Body](http://brm.io/matter-js/docs/classes/Body.html)
* `rotation`
  [Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)
* `[point]`
  [Vector](http://brm.io/matter-js/docs/classes/Vector.html)
  optional

@

[`src/body/Body.js:490`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l490)

### Matter.Body.[scale](http://brm.io/matter-js/docs/classes/Body.html#method_scale)

\(

body

,

scaleX

,

scaleY

,

\[point\]

\)



Scales the body, including updating physical properties \(mass, area, axes, inertia\), from a world-space point \(default is body centre\).

#### Parameters

* `body`
  [Body](http://brm.io/matter-js/docs/classes/Body.html)
* `scaleX`
  [Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)
* `scaleY`
  [Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)
* `[point]`
  [Vector](http://brm.io/matter-js/docs/classes/Vector.html)
  optional

@

[`src/body/Body.js:515`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l515)

### Matter.Body.[set](http://brm.io/matter-js/docs/classes/Body.html#method_set)

\(

body

,

settings

,

value

\)



Given a property and a value \(or map of\), sets the property\(s\) on the body, using the appropriate setter functions if they exist. Prefer to use the actual setter functions in performance critical situations.

#### Parameters

* `body`
  [Body](http://brm.io/matter-js/docs/classes/Body.html)
* `settings`
  [Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)
  A property name \(or map of properties and values\) to set on the body.

* `value`
  [Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)
  The value to set if`settings`is a single property name.

@

[`src/body/Body.js:164`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l164)

### Matter.Body.[setAngle](http://brm.io/matter-js/docs/classes/Body.html#method_setAngle)

\(

body

,

angle

\)



Sets the angle of the body instantly. Angular velocity, position, force etc. are unchanged.

#### Parameters

* `body`
  [Body](http://brm.io/matter-js/docs/classes/Body.html)
* `angle`
  [Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)

@

[`src/body/Body.js:432`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l432)

### Matter.Body.[setAngularVelocity](http://brm.io/matter-js/docs/classes/Body.html#method_setAngularVelocity)

\(

body

,

velocity

\)



Sets the angular velocity of the body instantly. Position, angle, force etc. are unchanged. See also`Body.applyForce`.

#### Parameters

* `body`
  [Body](http://brm.io/matter-js/docs/classes/Body.html)
* `velocity`
  [Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)

@

[`src/body/Body.js:468`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l468)

### Matter.Body.[setDensity](http://brm.io/matter-js/docs/classes/Body.html#method_setDensity)

\(

body

,

density

\)



Sets the density of the body. Mass is automatically updated to reflect the change.

#### Parameters

* `body`
  [Body](http://brm.io/matter-js/docs/classes/Body.html)
* `density`
  [Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)

@

[`src/body/Body.js:289`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l289)

### Matter.Body.[setInertia](http://brm.io/matter-js/docs/classes/Body.html#method_setInertia)

\(

body

,

inertia

\)



Sets the moment of inertia \(i.e. second moment of area\) of the body of the body. Inverse inertia is automatically updated to reflect the change. Mass is not changed.

#### Parameters

* `body`
  [Body](http://brm.io/matter-js/docs/classes/Body.html)
* `inertia`
  [Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)

@

[`src/body/Body.js:300`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l300)

### Matter.Body.[setMass](http://brm.io/matter-js/docs/classes/Body.html#method_setMass)

\(

body

,

mass

\)



Sets the mass of the body. Inverse mass and density are automatically updated to reflect the change.

#### Parameters

* `body`
  [Body](http://brm.io/matter-js/docs/classes/Body.html)
* `mass`
  [Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)

@

[`src/body/Body.js:277`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l277)

### Matter.Body.[setParts](http://brm.io/matter-js/docs/classes/Body.html#method_setParts)

\(

body

,

\[body\]

,

\[autoHull=true\]

\)



Sets the parts of the`body`and updates mass, inertia and centroid. Each part will have its parent set to`body`. By default the convex hull will be automatically computed and set on`body`, unless`autoHull`is set to`false.`Note that this method will ensure that the first part in`body.parts`will always be the`body`.

#### Parameters

* `body`
  [Body](http://brm.io/matter-js/docs/classes/Body.html)
* `[body]`
  [Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)
  optional
  parts

* `[autoHull=true]`
  Bool
  optional

@

[`src/body/Body.js:349`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l349)

### Matter.Body.[setPosition](http://brm.io/matter-js/docs/classes/Body.html#method_setPosition)

\(

body

,

position

\)



Sets the position of the body instantly. Velocity, angle, force etc. are unchanged.

#### Parameters

* `body`
  [Body](http://brm.io/matter-js/docs/classes/Body.html)
* `position`
  [Vector](http://brm.io/matter-js/docs/classes/Vector.html)

@

[`src/body/Body.js:412`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l412)

### Matter.Body.[setStatic](http://brm.io/matter-js/docs/classes/Body.html#method_setStatic)

\(

body

,

isStatic

\)



Sets the body as static, including isStatic flag and setting mass and inertia to Infinity.

#### Parameters

* `body`
  [Body](http://brm.io/matter-js/docs/classes/Body.html)
* `isStatic`
  Bool

@

[`src/body/Body.js:229`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l229)

### Matter.Body.[setVelocity](http://brm.io/matter-js/docs/classes/Body.html#method_setVelocity)

\(

body

,

velocity

\)



Sets the linear velocity of the body instantly. Position, angle, force etc. are unchanged. See also`Body.applyForce`.

#### Parameters

* `body`
  [Body](http://brm.io/matter-js/docs/classes/Body.html)
* `velocity`
  [Vector](http://brm.io/matter-js/docs/classes/Vector.html)

@

[`src/body/Body.js:454`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l454)

### Matter.Body.[setVertices](http://brm.io/matter-js/docs/classes/Body.html#method_setVertices)

\(

body

,

vertices

\)



Sets the body's vertices and updates body properties accordingly, including inertia, area and mass \(with respect to`body.density`\). Vertices will be automatically transformed to be orientated around their centre of mass as the origin. They are then automatically translated to world space based on`body.position`.

The`vertices`argument should be passed as an array of`Matter.Vector`points \(or a`Matter.Vertices`array\). Vertices must form a convex hull, concave hulls are not supported.

#### Parameters

* `body`
  [Body](http://brm.io/matter-js/docs/classes/Body.html)
* `vertices`
  [Vector\[\]](http://brm.io/matter-js/docs/classes/Vector.html)

@

[`src/body/Body.js:312`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l312)

### Matter.Body.[translate](http://brm.io/matter-js/docs/classes/Body.html#method_translate)

\(

body

,

translation

\)



Moves a body by a given vector relative to its current position, without imparting any velocity.

#### Parameters

* `body`
  [Body](http://brm.io/matter-js/docs/classes/Body.html)
* `translation`
  [Vector](http://brm.io/matter-js/docs/classes/Vector.html)

@

[`src/body/Body.js:480`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l480)

### Matter.Body.[update](http://brm.io/matter-js/docs/classes/Body.html#method_update)

\(

body

,

deltaTime

,

timeScale

,

correction

\)



Performs a simulation step for the given`body`, including updating position and angle using Verlet integration.

#### Parameters

* `body`
  [Body](http://brm.io/matter-js/docs/classes/Body.html)
* `deltaTime`
  [Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)
* `timeScale`
  [Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)
* `correction`
  [Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)

@

[`src/body/Body.js:565`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l565)

## Properties

The following properties are specified for objects created by`Matter.Body.create`and for objects passed to it via the`options`argument.

### body.[`angle`](http://brm.io/matter-js/docs/classes/Body.html#property_angle)

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)



A`Number`specifying the angle of the body, in radians.

Default:`0`

@

[`src/body/Body.js:755`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l755)

### body.[`angularSpeed`](http://brm.io/matter-js/docs/classes/Body.html#property_angularSpeed)

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)



A`Number`that_measures_the current angular speed of the body after the last`Body.update`. It is read-only and always positive \(it's the magnitude of`body.angularVelocity`\).

Default:`0`

@

[`src/body/Body.js:812`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l812)

### body.[`angularVelocity`](http://brm.io/matter-js/docs/classes/Body.html#property_angularVelocity)

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)



A`Number`that_measures_the current angular velocity of the body after the last`Body.update`. It is read-only. If you need to modify a body's angular velocity directly, you should apply a torque or simply change the body's`angle`\(as the engine uses position-Verlet integration\).

Default:`0`

@

[`src/body/Body.js:831`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l831)

### body.[`area`](http://brm.io/matter-js/docs/classes/Body.html#property_area)

[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)



A`Number`that_measures_the area of the body's convex hull, calculated at creation by`Body.create`.

@

[`src/body/Body.js:1158`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l1158)

### body.[`axes`](http://brm.io/matter-js/docs/classes/Body.html#property_axes)

[Vector\[\]](http://brm.io/matter-js/docs/classes/Vector.html)



An array of unique axis vectors \(edge normals\) used for collision detection. These are automatically calculated from the given convex hull \(`vertices`array\) in`Body.create`. They are constantly updated by`Body.update`during the simulation.

@

[`src/body/Body.js:1149`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l1149)

### body.[`bounds`](http://brm.io/matter-js/docs/classes/Body.html#property_bounds)

[Bounds](http://brm.io/matter-js/docs/classes/Bounds.html)



A`Bounds`object that defines the AABB region for the body. It is automatically calculated from the given convex hull \(`vertices`array\) in`Body.create`and constantly updated by`Body.update`during simulation.

@

[`src/body/Body.js:1166`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l1166)

### body.[`collisionFilter`](http://brm.io/matter-js/docs/classes/Body.html#property_collisionFilter)

[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)



An`Object`that specifies the collision filtering properties of this body.

Collisions between two bodies will obey the following rules:

* If the two bodies have the same non-zero value of
  `collisionFilter.group`
  , they will always collide if the value is positive, and they will never collide if the value is negative.
* If the two bodies have different values of
  `collisionFilter.group`
  or if one \(or both\) of the bodies has a value of 0, then the category/mask rules apply as follows:

Each body belongs to a collision category, given by`collisionFilter.category`. This value is used as a bit field and the category should have only one bit set, meaning that the value of this property is a power of two in the range \[1, 2^31\]. Thus, there are 32 different collision categories available.

Each body also defines a collision bitmask, given by`collisionFilter.mask`which specifies the categories it collides with \(the value is the bitwise AND value of all these categories\).

Using the category/mask rules, two bodies`A`and`B`collide if each includes the other's category in its mask, i.e.`(categoryA & maskB) !== 0`and`(categoryB & maskA) !== 0`are both true.

@

[`src/body/Body.js:980`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l980)

### body.[`collisionFilter.category`](http://brm.io/matter-js/docs/classes/Body.html#property_collisionFilter.category)

[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)



A bit field that specifies the collision category this body belongs to. The category value should have only one bit set, for example`0x0001`. This means there are up to 32 unique collision categories available. See`body.collisionFilter`for more information.

Default:`1`

@

[`src/body/Body.js:1015`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l1015)

### body.[`collisionFilter.group`](http://brm.io/matter-js/docs/classes/Body.html#property_collisionFilter.group)

[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)



An Integer`Number`, that specifies the collision group this body belongs to. See`body.collisionFilter`for more information.

Default:`0`

@

[`src/body/Body.js:1006`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l1006)

### body.[`collisionFilter.mask`](http://brm.io/matter-js/docs/classes/Body.html#property_collisionFilter.mask)

[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)



A bit mask that specifies the collision categories this body may collide with. See`body.collisionFilter`for more information.

Default:`-1`

@

[`src/body/Body.js:1026`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l1026)

### body.[`density`](http://brm.io/matter-js/docs/classes/Body.html#property_density)

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)



A`Number`that defines the density of the body, that is its mass per unit area. If you pass the density via`Body.create`the`mass`property is automatically calculated for you based on the size \(area\) of the object. This is generally preferable to simply setting mass and allows for more intuitive definition of materials \(e.g. rock has a higher density than wood\).

Default:`0.001`

@

[`src/body/Body.js:885`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l885)

### body.[`force`](http://brm.io/matter-js/docs/classes/Body.html#property_force)

[Vector](http://brm.io/matter-js/docs/classes/Vector.html)



A`Vector`that specifies the force to apply in the current step. It is zeroed after every`Body.update`. See also`Body.applyForce`.

Default:`{ x: 0, y: 0 }`

@

[`src/body/Body.js:787`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l787)

### body.[`friction`](http://brm.io/matter-js/docs/classes/Body.html#property_friction)

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)



A`Number`that defines the friction of the body. The value is always positive and is in the range`(0, 1)`. A value of`0`means that the body may slide indefinitely. A value of`1`means the body may come to a stop almost instantly after a force is applied.

The effects of the value may be non-linear. High values may be unstable depending on the body. The engine uses a Coulomb friction model including static and kinetic friction. Note that collision response is based on_pairs_of bodies, and that`friction`values are_combined_with the following formula:

```
Math
.
min
(
bodyA
.
friction
,
 bodyB
.
friction
)
```

Default:`0.1`

@

[`src/body/Body.js:941`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l941)

### body.[`frictionAir`](http://brm.io/matter-js/docs/classes/Body.html#property_frictionAir)

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)



A`Number`that defines the air friction of the body \(air resistance\). A value of`0`means the body will never slow as it moves through space. The higher the value, the faster a body slows when moving through space. The effects of the value are non-linear.

Default:`0.01`

@

[`src/body/Body.js:969`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l969)

### body.[`frictionStatic`](http://brm.io/matter-js/docs/classes/Body.html#property_frictionStatic)

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)



A`Number`that defines the static friction of the body \(in the Coulomb friction model\). A value of`0`means the body will never 'stick' when it is nearly stationary and only dynamic`friction`is used. The higher the value \(e.g.`10`\), the more force it will take to initially get the body moving when nearly stationary. This value is multiplied with the`friction`property to make it easier to change`friction`and maintain an appropriate amount of static friction.

Default:`0.5`

@

[`src/body/Body.js:958`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l958)

### body.[`id`](http://brm.io/matter-js/docs/classes/Body.html#property_id)

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)



An integer`Number`uniquely identifying number generated in`Body.create`by`Common.nextId`.

@

[`src/body/Body.js:703`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l703)

### body.[`inertia`](http://brm.io/matter-js/docs/classes/Body.html#property_inertia)

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)



A`Number`that defines the moment of inertia \(i.e. second moment of area\) of the body. It is automatically calculated from the given convex hull \(`vertices`array\) and density in`Body.create`. If you modify this value, you must also modify the`body.inverseInertia`property \(`1 / inertia`\).

@

[`src/body/Body.js:911`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l911)

### body.[`inverseInertia`](http://brm.io/matter-js/docs/classes/Body.html#property_inverseInertia)

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)



A`Number`that defines the inverse moment of inertia of the body \(`1 / inertia`\). If you modify this value, you must also modify the`body.inertia`property.

@

[`src/body/Body.js:920`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l920)

### body.[`inverseMass`](http://brm.io/matter-js/docs/classes/Body.html#property_inverseMass)

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)



A`Number`that defines the inverse mass of the body \(`1 / mass`\). If you modify this value, you must also modify the`body.mass`property.

@

[`src/body/Body.js:903`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l903)

### body.[`isSensor`](http://brm.io/matter-js/docs/classes/Body.html#property_isSensor)

[Boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)



A flag that indicates whether a body is a sensor. Sensor triggers collision events, but doesn't react with colliding body physically.

Default:`false`

@

[`src/body/Body.js:850`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l850)

### body.[`isSleeping`](http://brm.io/matter-js/docs/classes/Body.html#property_isSleeping)

[Boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)



A flag that indicates whether the body is considered sleeping. A sleeping body acts similar to a static body, except it is only temporary and can be awoken. If you need to set a body as sleeping, you should use`Sleeping.set`as this requires more than just setting this flag.

Default:`false`

@

[`src/body/Body.js:858`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l858)

### body.[`isStatic`](http://brm.io/matter-js/docs/classes/Body.html#property_isStatic)

[Boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)



A flag that indicates whether a body is considered static. A static body can never change position or angle and is completely fixed. If you need to set a body as static after its creation, you should use`Body.setStatic`as this requires more than just setting this flag.

Default:`false`

@

[`src/body/Body.js:841`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l841)

### body.[`label`](http://brm.io/matter-js/docs/classes/Body.html#property_label)

[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)



An arbitrary`String`name to help the user identify and manage bodies.

Default:`"Body"`

@

[`src/body/Body.js:719`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l719)

### body.[`mass`](http://brm.io/matter-js/docs/classes/Body.html#property_mass)

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)



A`Number`that defines the mass of the body, although it may be more appropriate to specify the`density`property instead. If you modify this value, you must also modify the`body.inverseMass`property \(`1 / mass`\).

@

[`src/body/Body.js:895`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l895)

### body.[`motion`](http://brm.io/matter-js/docs/classes/Body.html#property_motion)

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)



A`Number`that_measures_the amount of movement a body currently has \(a combination of`speed`and`angularSpeed`\). It is read-only and always positive. It is used and updated by the`Matter.Sleeping`module during simulation to decide if a body has come to rest.

Default:`0`

@

[`src/body/Body.js:867`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l867)

### body.[`parent`](http://brm.io/matter-js/docs/classes/Body.html#property_parent)

[Body](http://brm.io/matter-js/docs/classes/Body.html)



A self reference if the body is_not_a part of another body. Otherwise this is a reference to the body that this is a part of. See`body.parts`.

@

[`src/body/Body.js:746`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l746)

### body.[`parts`](http://brm.io/matter-js/docs/classes/Body.html#property_parts)

[Body\[\]](http://brm.io/matter-js/docs/classes/Body.html)



An array of bodies that make up this body. The first body in the array must always be a self reference to the current body instance. All bodies in the`parts`array together form a single rigid compound body. Parts are allowed to overlap, have gaps or holes or even form concave bodies. Parts themselves should never be added to a`World`, only the parent body should be. Use`Body.setParts`when setting parts to ensure correct updates of all properties.

@

[`src/body/Body.js:727`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l727)

### body.[`plugin`](http://brm.io/matter-js/docs/classes/Body.html#property_plugin)



An object reserved for storing plugin-specific properties.

@

[`src/body/Body.js:739`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l739)

### body.[`position`](http://brm.io/matter-js/docs/classes/Body.html#property_position)

[Vector](http://brm.io/matter-js/docs/classes/Vector.html)



A`Vector`that specifies the current world-space position of the body.

Default:`{ x: 0, y: 0 }`

@

[`src/body/Body.js:779`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l779)

### body.[`render`](http://brm.io/matter-js/docs/classes/Body.html#property_render)

[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)



An`Object`that defines the rendering properties to be consumed by the module`Matter.Render`.

@

[`src/body/Body.js:1053`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l1053)

### body.[`render.fillStyle`](http://brm.io/matter-js/docs/classes/Body.html#property_render.fillStyle)

[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)



A`String`that defines the fill style to use when rendering the body \(if a sprite is not defined\). It is the same as when using a canvas, so it accepts CSS style property values.

Default:`a random colour`

@

[`src/body/Body.js:1131`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l1131)

### body.[`render.lineWidth`](http://brm.io/matter-js/docs/classes/Body.html#property_render.lineWidth)

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)



A`Number`that defines the line width to use when rendering the body outline \(if a sprite is not defined\). A value of`0`means no outline will be rendered.

Default:`0`

@

[`src/body/Body.js:1122`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l1122)

### body.[`render.opacity`](http://brm.io/matter-js/docs/classes/Body.html#property_render.opacity)

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)



Sets the opacity to use when rendering.

Default:`1`

@

[`src/body/Body.js:1068`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l1068)

### body.[`render.sprite`](http://brm.io/matter-js/docs/classes/Body.html#property_render.sprite)

[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)



An`Object`that defines the sprite properties to use when rendering, if any.

@

[`src/body/Body.js:1076`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l1076)

### body.[`render.sprite.texture`](http://brm.io/matter-js/docs/classes/Body.html#property_render.sprite.texture)

[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)



An`String`that defines the path to the image to use as the sprite texture, if any.

@

[`src/body/Body.js:1083`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l1083)

### body.[`render.sprite.xOffset`](http://brm.io/matter-js/docs/classes/Body.html#property_render.sprite.xOffset)

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)



A`Number`that defines the offset in the x-axis for the sprite \(normalised by texture width\).

Default:`0`

@

[`src/body/Body.js:1106`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l1106)

### body.[`render.sprite.xScale`](http://brm.io/matter-js/docs/classes/Body.html#property_render.sprite.xScale)

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)



A`Number`that defines the scaling in the x-axis for the sprite, if any.

Default:`1`

@

[`src/body/Body.js:1090`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l1090)

### body.[`render.sprite.yOffset`](http://brm.io/matter-js/docs/classes/Body.html#property_render.sprite.yOffset)

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)



A`Number`that defines the offset in the y-axis for the sprite \(normalised by texture height\).

Default:`0`

@

[`src/body/Body.js:1114`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l1114)

### body.[`render.sprite.yScale`](http://brm.io/matter-js/docs/classes/Body.html#property_render.sprite.yScale)

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)



A`Number`that defines the scaling in the y-axis for the sprite, if any.

Default:`1`

@

[`src/body/Body.js:1098`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l1098)

### body.[`render.strokeStyle`](http://brm.io/matter-js/docs/classes/Body.html#property_render.strokeStyle)

[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)



A`String`that defines the stroke style to use when rendering the body outline \(if a sprite is not defined\). It is the same as when using a canvas, so it accepts CSS style property values.

Default:`a random colour`

@

[`src/body/Body.js:1140`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l1140)

### body.[`render.visible`](http://brm.io/matter-js/docs/classes/Body.html#property_render.visible)

[Boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)



A flag that indicates if the body should be rendered.

Default:`true`

@

[`src/body/Body.js:1060`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l1060)

### body.[`restitution`](http://brm.io/matter-js/docs/classes/Body.html#property_restitution)

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)



A`Number`that defines the restitution \(elasticity\) of the body. The value is always positive and is in the range`(0, 1)`. A value of`0`means collisions may be perfectly inelastic and no bouncing may occur. A value of`0.8`means the body may bounce back with approximately 80% of its kinetic energy. Note that collision response is based on_pairs_of bodies, and that`restitution`values are_combined_with the following formula:

```
Math
.
max
(
bodyA
.
restitution
,
 bodyB
.
restitution
)
```

Default:`0`

@

[`src/body/Body.js:928`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l928)

### body.[`sleepThreshold`](http://brm.io/matter-js/docs/classes/Body.html#property_sleepThreshold)

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)



A`Number`that defines the number of updates in which this body must have near-zero velocity before it is set as sleeping by the`Matter.Sleeping`module \(if sleeping is enabled by the engine\).

Default:`60`

@

[`src/body/Body.js:877`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l877)

### body.[`slop`](http://brm.io/matter-js/docs/classes/Body.html#property_slop)

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)



A`Number`that specifies a tolerance on how far a body is allowed to 'sink' or rotate into other bodies. Avoid changing this value unless you understand the purpose of`slop`in physics engines. The default should generally suffice, although very large bodies may require larger values for stable stacking.

Default:`0.05`

@

[`src/body/Body.js:1035`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l1035)

### body.[`speed`](http://brm.io/matter-js/docs/classes/Body.html#property_speed)

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)



A`Number`that_measures_the current speed of the body after the last`Body.update`. It is read-only and always positive \(it's the magnitude of`body.velocity`\).

Default:`0`

@

[`src/body/Body.js:803`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l803)

### body.[`timeScale`](http://brm.io/matter-js/docs/classes/Body.html#property_timeScale)

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)



A`Number`that allows per-body time scaling, e.g. a force-field where bodies inside are in slow-motion, while others are at full speed.

Default:`1`

@

[`src/body/Body.js:1045`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l1045)

### body.[`torque`](http://brm.io/matter-js/docs/classes/Body.html#property_torque)

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)



A`Number`that specifies the torque \(turning force\) to apply in the current step. It is zeroed after every`Body.update`.

Default:`0`

@

[`src/body/Body.js:795`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l795)

### body.[`type`](http://brm.io/matter-js/docs/classes/Body.html#property_type)

[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)



A`String`denoting the type of object.

Default:`"body"`

@

[`src/body/Body.js:710`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l710)

### body.[`velocity`](http://brm.io/matter-js/docs/classes/Body.html#property_velocity)

[Vector](http://brm.io/matter-js/docs/classes/Vector.html)



A`Vector`that_measures_the current velocity of the body after the last`Body.update`. It is read-only. If you need to modify a body's velocity directly, you should either apply a force or simply change the body's`position`\(as the engine uses position-Verlet integration\).

Default:`{ x: 0, y: 0 }`

@

[`src/body/Body.js:821`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l821)

### body.[`vertices`](http://brm.io/matter-js/docs/classes/Body.html#property_vertices)

[Vector\[\]](http://brm.io/matter-js/docs/classes/Vector.html)



An array of`Vector`objects that specify the convex hull of the rigid body. These should be provided about the origin`(0, 0)`. E.g.

```
[{
 x
:
0
,
 y
:
0
},
{
 x
:
25
,
 y
:
50
},
{
 x
:
50
,
 y
:
0
}]
```

When passed via`Body.create`, the vertices are translated relative to`body.position`\(i.e. world-space, and constantly updated by`Body.update`during simulation\). The`Vector`objects are also augmented with additional properties required for efficient collision detection.

Other properties such as`inertia`and`bounds`are automatically calculated from the passed vertices \(unless provided via`options`\). Concave hulls are not currently supported. The module`Matter.Vertices`contains useful methods for working with vertices.

@

[`src/body/Body.js:763`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l763)

## Events

The following events are emitted by objects created by`<span class="prefix">Matter.</span>Body.create`to objects that have subscribed using`Matter.Events.on`.

### Events.on\(body, "[`sleepEnd`](http://brm.io/matter-js/docs/classes/Body.html#event_sleepEnd)", callback\)



FireMatter.Bodyd when a body ends sleeping \(where`this`is the body\).

#### Event Payload:

* `event`
  [Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)
  An event object

  * `source`
    The source object of the event

  * `name`
    The name of the event

@

[`src/body/Body.js:687`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l687)

### Events.on\(body, "[`sleepStart`](http://brm.io/matter-js/docs/classes/Body.html#event_sleepStart)", callback\)



Fired when a body starts sleeping \(where`this`is the body\).

#### Event Payload:

* `event`
  [Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)
  An event object

  * `source`
    The source object of the event

  * `name`
    The name of the event

@

[`src/body/Body.js:677`](http://brm.io/matter-js/docs/files/src_body_Body.js.html#l677)

