---
title: Sobre unidades de medida (Referência do Visio ShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251828
localization_priority: Normal
ms.assetid: 48f765a8-7485-03c0-3484-d4ec07822600
description: Ao inserir campos no texto ou criar fórmulas, geralmente você especifica as unidades de medida para os valores digitados.
ms.openlocfilehash: d23c3f30841c81d07c09e57c0802e09edb0fe3c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360449"
---
# <a name="about-units-of-measure-visio-shapesheet-reference"></a>Sobre unidades de medida (Referência do Visio ShapeSheet)

Ao inserir campos no texto ou criar fórmulas, geralmente você especifica as unidades de medida para os valores digitados.
  
O Microsoft Visio avalia o resultado de uma fórmula de maneira diferente dependendo da célula na qual você digita a fórmula. Em geral, as células que representam a posição da forma, uma dimensão ou um ângulo exigem um par número-unidade que consiste em um número e nas unidades qualificadoras necessárias para interpretar o número. Muitas outras células não exigem unidades e são avaliadas como uma cadeia de caracteres, como VERDADEIRO ou FALSO ou como um índice. Por exemplo, a mesma fórmula que, na célula **FillForegnd**, significa cor 5 da paleta de cores do desenho significa TRUE (e bloqueia a largura da forma) na célula LockWidth. 
  
Sempre especifique uma unidade de medida quando você inserir uma fórmula em uma célula que espera um valor dimensional. Se não especificar uma unidade de medida, o Visio usará a unidade padrão para aquela célula, que pode ser unidades de página, desenho, texto, duração ou ângulo.
  
## <a name="units-of-measure"></a>Unidades de medida

Ao indicar unidades de medida em fórmulas do ShapeSheet, use as abreviações listadas na seguinte tabela.
  
|**Para especificar essas unidades de medida**|**Usar**|**Constante de automação**|
|:-----|:-----|:-----|
| Centímetros  <br/> | cm  <br/> |**visCentimeters (69)** <br/> |
| Cíceros  <br/> | c  <br/> |**visCiceros (54)** <br/> |
| Data ou hora  <br/> | data  <br/> |**visDate (40)** <br/> |
| Graus  <br/> | graus  <br/> |**visDegrees (81)** <br/> |
| Didots  <br/> | d  <br/> |**visDidots (53)** <br/> |
| Semanas decorridas  <br/> | sd  <br/> |**visElapsedWeek (43)** <br/> |
| Dias decorridos  <br/> | dd  <br/> |**visElapsedDay (44)** <br/> |
| Horas decorridas  <br/> | hd  <br/> |**visElapsedHour (45)** <br/> |
| Minutos decorridos  <br/> | md  <br/> |**visElapsedMin (46)** <br/> |
| Segundos decorridos  <br/> | sd  <br/> |**visElapsedSec (47)** <br/> |
| Pés  <br/> | ft  <br/> |**visFeet (66)** <br/> |
| Polegadas  <br/> | pol  <br/> |**visInches (65)** <br/> |
| Quilômetros  <br/> | km  <br/> |**visKilometers (72)** <br/> |
| Metros  <br/> | m  <br/> |**visMeters (71)** <br/> |
| Milhas  <br/> | mi  <br/> |**visMiles (68)** <br/> |
| Milímetros  <br/> | mm  <br/> |**visMillimeters (70)** <br/> |
| Minutos  <br/> | '  <br/> |**visMin (84)** <br/> |
| Milhas náuticas  <br/> | mn  <br/> |**visNautMiles (76)** <br/> |
| Porcentagem  <br/> | %  <br/> |**visPercent (33)** <br/> |
| Paica  <br/> | p  <br/> |**visPicas (51)** <br/> |
| Pontos  <br/> | pt  <br/> |**visPoints (50)** <br/> |
| Radianos  <br/> | rad  <br/> |**visRadians (83)** <br/> |
| Segundos  <br/> | "  <br/> |**visSec (85)** <br/> |
| Jardas  <br/> | yd  <br/> |**visYards (75)** <br/> |
   
## <a name="compound-units-of-measure"></a>Unidades de medida compostas

Em fórmulas, você pode expressar unidades de medida para números compostos usando as abreviações na seguinte tabela. O Visio simplifica os resultados e os exibe nas unidades compostas.
  
Por exemplo, se você inserir 45,635°, o Visio exibirá o valor equivalente a 45° 38' 6".
  
|**Para especificar unidades**|**Use esta abreviação**|**Constante de automação**|
|:-----|:-----|:-----|
| Cíceros e didots  <br/> | CÍCERO/DIDOT  <br/> |**visCicerosAndDidots (52)** <br/> |
| Graus, minutos e segundos  <br/> | °  <br/> |**visDegreeMinSec (82)** <br/> |
| Pés e polegadas  <br/> | PÉS/POL  <br/> |**visFeetAndInches (67)** <br/> |
| Paicas e pontos  <br/> | P e P  <br/> |**visPicasAndPoints (49)** <br/> |
   
## <a name="fractional-units-of-measure"></a>Unidades de medida fracionárias

Você pode especificar unidades de medidas fracionárias na célula **DrawingScale** para afetar o número de subdivisões de régua que o Visio exibe na janela de desenho. Por padrão, o Visio divide as distâncias em décimos ao desenhar suas réguas. Se você usar unidades de medidas fracionárias na célula **DrawingScale**, o Visio dividirá a distância da seguinte forma: 
  
- Oitavos para *visInchFrac* e *visMileFrac* 
    
- Duodécimos para *visFeetAndInches* 
    
As unidades fracionadas de medida não têm efeito em outras células que não na célula DrawingScale.
  
|**Para especificar unidades fracionárias**|**Use esta abreviação**|**Constante de automação**|
|:-----|:-----|:-----|
| Polegadas em frações  <br/> | IN_F  <br/> |**visInchFrac (73)** <br/> |
| Milhas em frações  <br/> | MI_F  <br/> |**visMileFrac (74)** <br/> |
| Pés e polegadas  <br/> | PÉS/POL  <br/> |**visFeetAndInches (67)** <br/> |
   
## <a name="multidimensional-units-of-measure"></a>Unidades multidimensionais de medida

Em fórmulas, você pode expressar unidades de medida para números multidimensionais usando as abreviações na seguinte tabela. O Visio simplifica os resultados e os exibe nas unidades multidimensionais.
  
|**Para especificar unidades multidimensionais**|**Use esta abreviação**|**Constante de automação**|
|:-----|:-----|:-----|
| Acre  <br/> | ACRES  <br/> |**visAcre (36)** <br/> |
| Centímetros  <br/> | CM2, CM2, CM.^2, CM^2  <br/> |**visCentimeters (69)** <br/> |
| Pés  <br/> | FT2, FT2, FT.^2, FT^2  <br/> |**visFeet (66)** <br/> |
| Hectare  <br/> | HECTARES, HECTARE, HA., HA  <br/> |**visHectare (37)** <br/> |
| Polegadas  <br/> | IN2, IN2, IN.^2, IN^2  <br/> |**visInches (65)** <br/> |
| Quilômetros  <br/> | KM2, KM2, KM.^2, KM ^2  <br/> |**visKilometers (72)** <br/> |
| Metros  <br/> | M2, M2, M.^2, M ^2  <br/> |**visMeters (71)** <br/> |
| Milhas  <br/> | MI2, MI2, MI.^2, MI ^2  <br/> |**visMiles (68)** <br/> |
| Milímetros  <br/> | MM2, MM2, MM.^2, MM ^2  <br/> |**visMillimeters (70)** <br/> |
| Jardas  <br/> | YD2, YD2, YD.^2, YD^2  <br/> |**visYards (75)** <br/> |
   
## <a name="universal-strings"></a>Seqûências de caracteres universais

Em versões localizadas do Visio, o conjunto de seqûências de caracteres reconhecidas muda com o idioma. Se deseja que seu programa funcione com vários idiomas, use as seqûências de caracteres universais para unidades de medida.
  
|**Para**|**Usar**|
|:-----|:-----|
| Centímetros  <br/> | CM  <br/> |
| Cíceros  <br/> | C  <br/> |
| Cíceros e didots  <br/> | CÍCERO/DIDOT  <br/> |
| Data ou hora  <br/> | DATA  <br/> |
| Graus  <br/> | GRAUS  <br/> |
| Graus, minutos e segundos  <br/> | °  <br/> |
| Didots  <br/> | D  <br/> |
| Semana decorrida  <br/> | SD  <br/> |
| Dia decorrido  <br/> | DD  <br/> |
| Hora decorrida  <br/> | HD  <br/> |
| Minuto decorrido  <br/> | MD  <br/> |
| Segundo decorrido  <br/> | SD  <br/> |
| Pés  <br/> | FT  <br/> |
| Pés e polegadas  <br/> | PÉS/POL  <br/> |
| Polegadas  <br/> | POL  <br/> |
| Polegadas em frações  <br/> | IN_F  <br/> |
| Quilômetros  <br/> | KM  <br/> |
| Metros  <br/> | M  <br/> |
| Milhas  <br/> | MI  <br/> |
| Milhas em frações  <br/> | MI_F  <br/> |
| Milímetros  <br/> | MM  <br/> |
| Minutos  <br/> | '  <br/> |
| Milhas náuticas  <br/> | MN  <br/> |
| Porcentagem  <br/> | %  <br/> |
| Paica  <br/> | P  <br/> |
| Paicas e pontos  <br/> | P e P  <br/> |
| Pontos  <br/> | PT  <br/> |
| Radianos  <br/> | RAD  <br/> |
| Segundos  <br/> | "  <br/> |
| Jardas  <br/> | YD  <br/> |
   
## <a name="implicit-units-of-measure"></a>Unidades implícitas de medida

Quando o Visio analisa e armazena um par de unidades numéricas, ele pode usar unidades explícitas ou implícitas. Um número expresso em unidades explícitas sempre é exibido nas unidades de medida originalmente inseridas. Um número expresso em unidades implícitas sempre é convertido para o valor equivalente no desenho, na página ou nas unidades angulares apropriadas para a célula.
  
Por exemplo, suponha que você insira o equivalente a 1 polegada na célula A usando unidades explícitas e na célula B usando unidades implícitas e ambas as células usam unidades de desenho. Em seguida, você altera as unidades padrão da página para centímetors. A célula A ainda exibe 1 pol., porque ela usa unidades explícitas que não são alteradas com o padrão. A célula B agora exibe 2,54 cm, o valor equivalente nas unidades padrão.
  
Para inserir unidades implicitamente, use a seguinte sintaxe.
  
```vb
number  [unit , flag ]
```

|||
|:-----|:-----|
| _número_ <br/> |O valor original, como 3,7, 1,7E-4 ou 5 1/2.  <br/> |
| _unidade_ <br/> |As unidades nas quais o _número_ é originalmente expresso.  <br/> |
| _sinalizador_ <br/> |O sistema de medida a ser usado quando a unidade de valor implícito é exibida. Veja abaixo para obter valores.  <br/> |
   
O _sinalizador_ de parâmetro é uma das seguintes letras (maiúsculas ou minúsculas) indicando o sistema de medição que deve ser usado quando a unidade de valor implícito é exibida. 
  
|**_Sinalizador_**|**Sistema de medida**|**Exemplo**|
|:-----|:-----|:-----|
| a, A  <br/> | Angular  <br/> | = 5 [graus, A]  <br/> |
| d, D  <br/> | Desenho  <br/> | = 5 [pol, D]  <br/> |
| e, E  <br/> | Duração  <br/> | = 5 [hd, E]  <br/> |
| p, P  <br/> | Página  <br/> | = 5 [pol, P]  <br/> |
| t, T  <br/> | Tipo  <br/> | = 5 [pt, T]  <br/> |
   
Além disso, você pode usar as unidades implícitas DL, DP, DT, DA, DE para unidades implícitas de desenho, página, texto, ângulo e tempo, respectivamente. Essas unidades supõem que o valor associado é de unidades internas. Por exemplo, se o sistema de medição atual é centímetros, *= 2 DL* seria interpretado como 2 unidades internas (polegadas) e exibido como 5,08 cm. 
  
Usando a sintaxe implícita descrita acima, esta expressão (=2 DL) é equivalente a 2[pol,d]. A sintaxe implícita oferece a você a opção de como interpretar o valor, então você também poderia especificar 2[pés,d], que seria interpretado como 2 pés e exibido como 60,96 cm. As unidades implícitas DL, DP, DT, DA e DE são universais e não possuem complementos localizados.
  
## <a name="default-units-of-measure"></a>Unidades padrão de medida

A seguir estão as unidades padrão de medida juntamente com suas configurações equivalentes na interface do usuário.
  
|**Unidade de medida padrão**|**Equivalente à interface do usuário**|
|:-----|:-----|
|**visDrawingUnits** <br/> |As unidades na célula DrawingScale da página ou mestre que contém a célula.  <br/> |
|**visPageUnits** <br/> |As unidades selecionadas na caixa **Unidades de medida** na guia **Propriedades da Página** da caixa de diálogo **Configuração da Página** (na guia **Design**, clique na seta **Configuração da Página**).  <br/> |
|**visTypeUnits** <br/> |As unidades selecionadas na caixa **Texto**, em **Exibir** na guia **Avançado** da caixa de diálogo **Opções do Visio** (clique na guia **Arquivo** e, em seguida, clique em **Opções**).  <br/> |
|**visAngleUnits** <br/> |As unidades selecionadas na caixa **Ângulo** em **Exibir** na guia **Avançado** da caixa de diálogo **Opções do Visio**.  <br/> |
|**visDurationUnits** <br/> |As unidades selecionadas na caixa **Duração** em **Exibir** na guia **Avançado** da caixa de diálogo **Opções do Visio**.  <br/> |
   

