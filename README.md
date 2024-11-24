
//using ports 10, 11, 12, 13
int relay1=10;
int relay2=11;
int relay3=12;
int relay4=13;
int val;

void setup() {
 
  Serial.begin(9600);
  pinMode(relay1,OUTPUT);
  pinMode(relay2,OUTPUT);
  pinMode(relay3,OUTPUT);
  pinMode(relay4,OUTPUT);
  digitalWrite(relay1,HIGH);
  digitalWrite(relay2,HIGH);
  digitalWrite(relay3,HIGH);
  digitalWrite(relay4,HIGH);

}
void loop() {
 
  //check data serial from bluetooth android App
  while (Serial.available() > 0){
    val = Serial.read();
    Serial.println(val);
  }
 
  //Relay is on
  if( val == 1 ) {
    digitalWrite(relay1,HIGH); }
  else if( val == 2 ) {
    digitalWrite(relay2,HIGH); }  else if( val == 3 ) {
    digitalWrite(relay3,HIGH); }
  else if( val == 4 ) {
    digitalWrite(relay4,HIGH); }
    
  //relay all on
  else if( val == 0 ) {
    digitalWrite(relay1,HIGH);
    digitalWrite(relay2,HIGH);
    digitalWrite(relay3,HIGH);
    digitalWrite(relay4,HIGH);
  }
  //relay is off
  else if( val == 5 ) {
    digitalWrite(relay1,LOW); }
  else if( val == 6 ) {
    digitalWrite(relay2,LOW); }
  else if( val == 7 ) {
    digitalWrite(relay3,LOW); }
  else if( val == 8 ) {
    digitalWrite(relay4,LOW); }
    
  //relay all off
  else if( val == 10 ) {
    digitalWrite(relay1,LOW);
    digitalWrite(relay2,LOW);
    digitalWrite(relay3,LOW);
    digitalWrite(relay4,LOW);
  }
}
```


<!--
**Gobika333/Gobika333** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
