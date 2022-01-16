import React from "react";
import ReactDOM from 'react-dom';
import './index.css';
import reportWebVitals from './reportWebVitals';

  

  let kierList = ["kierA", "kier2", "kier3", "kier4", "kier5", "kier6", "kier7", "kier8", "kier9", "kier10", "kierJ", "kierQ", "kierK"];
  let karoList = ["karoA", "karo2", "karo3", "karo4", "karo5", "karo6", "karo7", "karo8", "karo9", "karo10", "karoJ", "karoQ", "karoK"];
  let pikList = ["pikA", "pik2", "pik3", "pik4", "pik5", "pik6", "pik7", "pik8", "pik9", "pik10", "pikJ", "pikQ", "pikK"];
  let treflList = ["treflA", "trefl2", "trefl3", "trefl4", "trefl5", "trefl6", "trefl7", "trefl8", "trefl9", "trefl10", "treflJ", "treflQ", "treflK"];

  let redRules = ["kier2", "karo2", "pik3", "trefl3", "kier3", "karo3", "pik4", "trefl4", "kier4", "karo4", "pik5", "trefl5", "kier5", "karo5", "pik6", "trefl6", "kier6", "karo6", "pik7", "trefl7", "kier7", "karo7", "pik8", "trefl8", "kier8", "karo8", "pik9", "trefl9", "kier9", "karo9", "pik10", "trefl10", "kier10", "karo10", "pikJ", "treflJ", "kierJ", "karoJ", "pikQ", "treflQ", "kierQ", "karoQ", "pikK", "treflK"];
  let blackRules = ["pik2", "trefl2", "kier3", "karo3", "pik3", "trefl3", "kier4", "karo4", "pik4", "trefl4", "kier5","karo5", "pik5", "trefl5", "kier6", "karo6", "pik6", "trefl6", "kier7", "karo7", "pik7", "trefl7", "kier8", "karo8","pik8", "trefl8", "kier9", "karo9", "pik9", "trefl9", "kier10", "karo10", "pik10", "trefl10", "kierJ", "karoJ", "pikJ","treflJ", "kierQ", "karoQ", "pikQ", "treflQ", "kierK", "karoK"];

  let list = ["kier2", "kier3", "kier4", "kier5", "kier6", "kier7", "kier8", "kier9", "kier10", "kierJ", "kierQ", "kierK", "kierA", "karo2", "karo3", "karo4", "karo5", "karo6", "karo7", "karo8", "karo9", "karo10", "karoJ", "karoQ", "karoK", "karoA", "pik2", "pik3", "pik4", "pik5", "pik6", "pik7", "pik8", "pik9", "pik10", "pikJ", "pikQ", "pikK", "pikA", "trefl2", "trefl3", "trefl4", "trefl5", "trefl6", "trefl7", "trefl8", "trefl9", "trefl10", "treflJ", "treflQ", "treflK", "treflA"];

  let karty;
  let cardsIndex = 0;
  let pikDone = 0;
  let treflDone = 0;
  let karoDone = 0;
  let kierDone = 0;
  let kierIdx = 0;
  let pikIdx = 0;
  let treflIdx = 0;
  let karoIdx = 0;
  let backCards = [[], [], [], [], [], []];
  let youWin;
  let element;
  let from;


  for(let i = 0; i < 10; i++)
  {
    for(let j = 0; j <= 51; j++)
    {
      const random = Math.floor(Math.random() * (51 - 0 + 1)) + 0;
      let temp = list[j];
      list[j] = list[random];
      list[random] = temp;
    }
  }

  let piles = [[[list[0]]], [[list[2]]], [[list[5]]], [[list[9]]], [[list[14]]], [[list[20]]], [[list[27]]], [], [], [], [], [[list[28]], [list[29]], [list[30]], [list[31]], [list[32]], [list[33]], [list[34]], [list[35]], [list[36]], [list[37]], [list[38]], [list[39]], [list[40]], [list[41]], [list[42]], [list[43]], [list[44]], [list[45]], [list[46]], [list[47]], [list[48]], [list[49]], [list[50]], [list[51]]], [[list[1]]], [[list[3]], [list[4]]], [[list[6]], [list[7]], [list[8]]], [[list[10]], [list[11]], [list[12]], [list[13]]], [[list[15]], [list[16]], [list[17]], [list[18]], [list[19]]], [[list[21]], [list[22]], [list[23]], [list[24]], [list[25]], [list[26]]]];

  

  function changeCardsIndex()
  {
    cardsIndex++;
    if(cardsIndex == (piles[11].length - 1))
    {
      cardsIndex = 0;
    }
    karty = change();
    update();
  }

  function showRules()
  {
    document.getElementById("rules").classList.toggle("show");
  }

  function win()
  {
    youWin = <div className="winBox"><h1>Wygraleś!</h1></div>;
    karty = change();
    update();
  }

  function showBack()
  {
    let lastIdx = -1;
    backCards = [[], [], [], [], [], []];
    for(let i = 0; i < 6; i++)
    {
      if(piles[i+1].length == 0)
      {
        let index = piles[i + 12].length;

        for(let j = 0; j < (index); j++)
        {
          if(piles[i + 12][j] != 0)
          {
            lastIdx = j;
          }
        }
        if(lastIdx != -1)
        {
          piles[i+1].push(piles[i + 12][lastIdx]);
          piles[i + 12][lastIdx] = 0;
        }
      }
    }

    for(let i = 0; i < 6; i++)
    {
      let index = piles[i + 12].length;

      for(let j = 0; j < (index); j++)
      {
        if(piles[i + 12][j] != 0)
        {
          backCards[i][j] = "cardBack";
        }
      }
    }

    karty = change();
    update();
  }

  function change()
  {
    return(
      <div>
        <div>
          <div>{youWin}</div>
          <button onClick={showRules}>Zasady</button>
          <div id="rules" className="show">
            <p>
              W Klondike gra się przy użyciu standardowej talii 52 kart, bez Jokerów. Po potasowaniu, od lewej do prawej kładzie się na stole siedem wachlarzowatych stosów kart. Od lewej do prawej, każda kupka zawiera jedną kartę więcej niż poprzednia. Pierwsza i najbardziej wysunięta w lewo kupka zawiera jedną odwróconą kartę, druga kupka zawiera dwie karty (jedna odwrócona, jedna odwrócona), trzecia trzy (dwie odwrócone, jedna odwrócona), i tak dalej, aż do siódmej kupki, która zawiera siedem kart (sześć odwróconych, jedna odwrócona). Najwyższa karta z każdej kupki jest odkrywana. Pozostałe karty tworzą zasoby i są umieszczane zakryte w lewym górnym rogu układu.
            </p>
          </div>
        </div>

        <div className="leftTopPile">
          <img src={require("./cards/cardBack.png")} alt="card" onClick={changeCardsIndex}/>
          {
            piles[11][cardsIndex].map((item, index) => 
            (
              <img src={require("./cards/" + item + ".png")} key={cardsIndex} alt="card" draggable onDragStart={(e)=>getElement(cardsIndex, "11")} />
            ))
          }
        </div>

        <div onDrop={(e)=>getDiv("0")} onDragOver={(e)=>over(e)} className="midPile1">
          <div className="pileBackground"></div>
          {
            piles[0].map((item, index) => 
            (
              <img src={require("./cards/" + item + ".png")} key={index} alt="card" draggable onDragStart={(e)=>getElement(index, "0")} />
            ))
          }
        </div>
        <div onDrop={(e)=>getDiv("1")} onDragOver={(e)=>over(e)} className="midPile2">
          <div className="pileBackground"></div>
          {
            backCards[0].map((item, index) =>
            (
              <img src={require("./cards/" + item + ".png")} alt="card" key={index} className="displayBack"/>
            ))
          }
          {
            piles[1].map((item, index) => 
            (
              <img src={require("./cards/" + item + ".png")} key={index} alt="card" draggable onDragStart={(e)=>getElement(index, "1")} />
            ))
          }
        </div>
        <div onDrop={(e)=>getDiv("2")} onDragOver={(e)=>over(e)} className="midPile3">
          <div className="pileBackground"></div>
          {
            backCards[1].map((item, index) =>
            (
              <img src={require("./cards/" + item + ".png")} alt="card" key={index} className="displayBack"/>
            ))
          }
          {
            piles[2].map((item, index) => 
            (
              <img src={require("./cards/" + item + ".png")} key={index} alt="card" draggable onDragStart={(e)=>getElement(index, "2")} />
            ))
          }
        </div>
        <div onDrop={(e)=>getDiv("3")} onDragOver={(e)=>over(e)} className="midPile4">
          <div className="pileBackground"></div>
          {
            backCards[2].map((item, index) =>
            (
              <img src={require("./cards/" + item + ".png")} alt="card" key={index} className="displayBack"/>
            ))
          }
          {
            piles[3].map((item, index) => 
            (
              <img src={require("./cards/" + item + ".png")} key={index} alt="card" draggable onDragStart={(e)=>getElement(index, "3")} />
            ))
          }
        </div>
        <div onDrop={(e)=>getDiv("4")} onDragOver={(e)=>over(e)} className="midPile5">
          <div className="pileBackground"></div>
          {
            backCards[3].map((item, index) =>
            (
              <img src={require("./cards/" + item + ".png")} alt="card" key={index} className="displayBack"/>
            ))
          }
          {
            piles[4].map((item, index) => 
            (
              <img src={require("./cards/" + item + ".png")} key={index} alt="card" draggable onDragStart={(e)=>getElement(index, "4")} />
            ))
          }
        </div>
        <div onDrop={(e)=>getDiv("5")} onDragOver={(e)=>over(e)} className="midPile6">
          <div className="pileBackground"></div>
          {
            backCards[4].map((item, index) =>
            (
              <img src={require("./cards/" + item + ".png")} alt="card" key={index} className="displayBack"/>
            ))
          }
          {
            piles[5].map((item, index) => 
            (
              <img src={require("./cards/" + item + ".png")} key={index} alt="card" draggable onDragStart={(e)=>getElement(index, "5")} />
            ))
          }
        </div>
        <div onDrop={(e)=>getDiv("6")} onDragOver={(e)=>over(e)} className="midPile7">
          <div className="pileBackground"></div>
          {
            backCards[5].map((item, index) =>
            (
              <img src={require("./cards/" + item + ".png")} alt="card" key={index} className="displayBack"/>
            ))
          }
          {
            piles[6].map((item, index) => 
            (
              <img src={require("./cards/" + item + ".png")} key={index} alt="card" draggable onDragStart={(e)=>getElement(index, "6")} />
            ))
          }
        </div>

        <div onDrop={(e)=>getDiv("7")} onDragOver={(e)=>over(e)} className="topPile1">
          {
            piles[7].map((item, index) => 
            (
              <img src={require("./cards/" + item + ".png")} key={index} alt="card" draggable onDragStart={(e)=>getElement(index, "7")} />
            ))
          }
        </div>
        <div onDrop={(e)=>getDiv("8")} onDragOver={(e)=>over(e)} className="topPile2">
          {
            piles[8].map((item, index) => 
            (
              <img src={require("./cards/" + item + ".png")} key={index} alt="card" draggable onDragStart={(e)=>getElement(index, "8")} />
            ))
          }
        </div>
        <div onDrop={(e)=>getDiv("9")} onDragOver={(e)=>over(e)} className="topPile3">
          {
            piles[9].map((item, index) => 
            (
              <img src={require("./cards/" + item + ".png")} key={index} alt="card" draggable onDragStart={(e)=>getElement(index, "9")} />
            ))
          }
        </div>
        <div onDrop={(e)=>getDiv("10")} onDragOver={(e)=>over(e)} className="topPile4">
          {
            piles[10].map((item, index) => 
            (
              <img src={require("./cards/" + item + ".png")} key={index} alt="card" draggable onDragStart={(e)=>getElement(index, "10")} />
            ))
          }
        </div>
      </div>
    )
  }

  const getElement = (index, divIndex) => 
  {
    element = index;
    from = divIndex;
  };

  const over = (e) => 
  {
    e.preventDefault();
  };

  const getDiv = (index) => 
  {
    let temp = piles[from].length;
    let rules = false;

    for(let i = 0; i <= 52; i+=4)
    {
      if((piles[from][element] == redRules[i]) || (piles[from][element] == redRules[i + 1]))
      {
        if((piles[index][piles[index].length - 1] == redRules[i + 2]) || (piles[index][piles[index].length - 1] == redRules[i + 3]))
        {
          rules = true;
        }
      }
      else if((piles[from][element] == blackRules[i]) || (piles[from][element] == blackRules[i + 1]))
      {
        if((piles[index][piles[index].length - 1] == blackRules[i + 2]) || (piles[index][piles[index].length - 1] == blackRules[i + 3]))
        {
          rules = true;
        }
      }
    }

    if((piles[from][element] == "kierK" || piles[from][element] == "pikK" || piles[from][element] == "treflK" || piles[from][element] == "karoK") && (piles[index].length == 0))
    {
      rules = true;
    }

    if(from != 11 && index < 7 && rules == true)
    {
      for(let i = element; i < (temp); i++)
      {
        piles[index].push(piles[from].splice(element, 1));
      }
    }
    else if(from >= 7 && from <= 10)
    {
      if(kierList[kierDone-1] == piles[from][element])
      kierDone--;
      else if(pikList[pikDone-1] == piles[from][element])
      pikDone--;
      else if(treflList[treflDone-1] == piles[from][element])
      treflDone--;
      else if(karoList[karoDone] == piles[from][element])
      karoDone--;
    }
    else if(index >= 7 && index <= 10)
    {
      if(kierList[kierDone] == piles[from][element] && (kierIdx == index || kierIdx == 0))
      {
        piles[index].push(piles[from].splice(element, 1));
        kierDone++;
        kierIdx = index;
        if(from == 11 && cardsIndex > 0)
        cardsIndex--;
      }
      else if(pikList[pikDone] == piles[from][element] && (pikIdx == index || pikIdx == 0))
      {
        piles[index].push(piles[from].splice(element, 1));
        pikDone++;
        pikIdx = index;
        if(from == 11 && cardsIndex > 0)
        cardsIndex--;
      }
      else if(treflList[treflDone] == piles[from][element] && (treflIdx == index || treflIdx == 0))
      {
        piles[index].push(piles[from].splice(element, 1));
        treflDone++;
        treflIdx = index;
        if(from == 11 && cardsIndex > 0)
        cardsIndex--;
      }
      else if(karoList[karoDone] == piles[from][element] && (karoIdx == index || karoIdx == 0))
      {
        piles[index].push(piles[from].splice(element, 1));
        karoDone++;
        karoIdx = index;
        if(from == 11 && cardsIndex > 0)
        cardsIndex--;
      }
    }
    else if(from == 11 && rules == true)
    {
      piles[index].push(piles[from].splice(element, 1));
      if(cardsIndex > 0)
      {
        cardsIndex--;
      }
    }

    if(treflDone == 13 && kierDone == 13 && pikDone == 13 && karoDone == 13)
    {
      win();
    }

    showBack();
    karty = change();
    update();
  };

showBack();
update();

function update()
{
  ReactDOM.render(
    karty,
    document.getElementById('root')
  );
}
reportWebVitals();
