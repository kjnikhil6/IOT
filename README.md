## Me
I'm NIKHIL KJ....

### Expt 1:LED Blinking
```c
int ledPin = 4;
void setup() {
  pinMode(ledPin,OUTPUT);
}

void loop() {
  digitalWrite(ledPin,HIGH);
  delay(1000);
  digitalWrite(ledPin,LOW);
  delay(1000);
}
```


<!-- blank line -->
<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/enMumwvLAug" frameborder="0" allowfullscreen="true"> </iframe>
</figure>
<!-- blank line -->
<iframe width="560" height="315"
src="https://www.youtube.com/embed/MUQfKFzIOeU" 
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

### Expt 2:Traffic Light

```c
int rLED = 13;
int yLED = 8;
int gLED = 2;
int i;
void setup() {
  pinMode(rLED,OUTPUT);
  pinMode(yLED,OUTPUT);
  pinMode(gLED,OUTPUT);
}

void loop() {
  digitalWrite(gLED,HIGH);
  delay(5000);
  digitalWrite(gLED,LOW);
  
  for(i=0;i<3;i++){
    delay(500);
    digitalWrite(yLED,HIGH);
    delay(500);
    digitalWrite(yLED,LOW);
  }
  delay(500);
  digitalWrite(rLED,HIGH);
  delay(5000);
  digitalWrite(rLED,LOW);
  
}
```

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/kjnikhil6/IoT/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.


