# **Anna Filatova**

### **Contacts**:
Discord: @Filannet  
Telegram: @lavenderann  
Email: filanna33@gmail.com  

### **About me**  
Hi! I’m a future junior frontend developer. I'm from Ukraine, but now I live in Georgia.  
My life changed a lot because of the war. Settled life and familiar work are in the past. But ahead is a chance 
to find myself in the completely new profession and realize my hidden talents. This is a real challenge, but it incredibly
motivates me not to stand still, but to boldly move forward.  
I am very responsible, goal-oriented and a good team player.  
I really like swimming and hiking. And I am ready to row and climb as hard as I can to become a real professional in my new field.  

### **Skills:**
    * HTML
    * CSS
    * SASS
    * Java Script
    * TypeScript
    * React
    * Git
    * BEM
    * Figma
    * Editors: WebStorm, VS Code  

### **Code example:**  
```
import React, {FC, useMemo, useState} from 'react';
import {Title} from "../index";
import './Portfolio.scss';

interface PortfolioItem {
    id: number,
    title: string,
    description: string,
    link: string,
    image: string,
    type: string
}

type Props = {
    items: Array<PortfolioItem>
}

const Portfolio: FC<Props> = ({items}) => {
    const [tab, setTab] = useState('all');
    const cards = useMemo(() => {
        return items.filter((item) => item.type === tab || tab === 'all');
    }, [items, tab]);

    return (
        <div className='portfolioWrapper' id='portfolio' data-testid='portfolio'>
            <Title title='Portfolio'/>
            <ul className='portfolioNavigation'>
                <li className={`portfolioNavigationItem ${tab === 'all' ? 'active' : ''}`} onClick={() => setTab('all')}>All</li>
                <li className={`portfolioNavigationItem ${tab === 'code' ? 'active' : ''}`} onClick={() => setTab('code')}>Code</li>
                <li className={`portfolioNavigationItem ${tab === 'ui' ? 'active' : ''}`} onClick={() => setTab('ui')}>UI</li>
            </ul>
            <div className='portfolioCards'>
                {cards?.map((card) => (
                    <div className='portfolioCard' key={card.id}>
                        <img className='portfolioCardImage' src={card.image} alt=''/>
                        <div className='portfolioCardContent'>
                            <h3 className='portfolioTitle'>{card.title}</h3>
                            <p className='portfolioDescription'>{card.description}</p>
                            <a className='portfolioLink' href={card.link} target='_blank' rel="noreferrer">View resource</a>
                        </div>
                    </div>
                ))}
            </div>
        </div>
    );
};

export default Portfolio;  
```


### **Education**  
**Volodymyr Dahl East Ukrainian National University**  
Faculty of Philosophy  
Specialty: *Psychology*  

**National Pedagogical University named after Taras Shevchenko**  
Department of Defectology and Psychological Correction. Center for Postgraduate Education  
Specialty: *Speech therapy*

### **Courses**  
**Creative&Tech Online Institute Projector**  
Web design scholarship  

**EPAM**  
Front-end Development (UpSkill b2b)  

### **Languages**  
    * ENGLISH  
      Upper-intermediate  

    * RUSSIAN  
      Native  

    * UKRAINIAN 
      Advanced  

### **Hobbies**  
    * Reading  
    * Hiking
    * Swimming
    * Nature photography






