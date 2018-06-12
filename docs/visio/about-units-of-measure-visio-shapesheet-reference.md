---
title: Sobre unidades de medida (referência de ShapeSheet do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251828
localization_priority: Normal
ms.assetid: 48f765a8-7485-03c0-3484-d4ec07822600
description: Quando você insere campos em texto ou cria fórmulas, com frequência especifica unidades de medida para os valores digitados.
ms.openlocfilehash: ce8ad1cdcbdaba713edeb06f4cd949e49f82a311
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771248"
---
# <a name="about-units-of-measure-visio-shapesheet-reference"></a>Sobre unidades de medida (referência de ShapeSheet do Visio)

Quando você insere campos em texto ou cria fórmulas, com frequência especifica unidades de medida para os valores digitados.
  
Microsoft Visio avalia o resultado de uma fórmula de forma diferente, dependendo da célula em que você inserir a fórmula. Em geral, as células que representa a posição da forma, uma dimensão ou um ângulo exigem um par de unidade numérica que consiste em um número e as unidades de qualificação necessárias para interpretar o número. Muitas outras células não precisam de unidades e avaliar como uma sequência de caracteres, como verdadeiro ou falso ou a um índice. Por exemplo, a mesma fórmula na célula **FillForegnd** isso significa que 5 de cores da paleta de cores do desenho significa TRUE (e bloqueia a largura da forma) na célula LockWidth. 
  
Sempre especifique uma unidade de medida quando você inserir uma fórmula em uma célula que espera um valor dimensional. Se não especificar uma unidade de medida, o Visio usará a unidade padrão para aquela célula, que pode ser unidades de página, desenho, texto, duração ou ângulo.
  
## <a name="units-of-measure"></a>Unidades de medida

Ao indicar unidades de medida em fórmulas ShapeSheet, use as abreviações listadas na tabela a seguir.
  
|**Para especificar essas unidades de medida**|**Uso**|**Constante de automação**|
|:-----|:-----|:-----|
| Centímetros  <br/> | cm  <br/> |**visCentimeters (69)** <br/> |
| Cíceros  <br/> | c  <br/> |**visCiceros (54)** <br/> |
| Data ou hora  <br/> | data  <br/> |**visDate (40)** <br/> |
| Graus  <br/> | gra  <br/> |**visDegrees (81)** <br/> |
| Didots  <br/> | d  <br/> |**visDidots (53)** <br/> |
| Semanas decorridas  <br/> | sd  <br/> |**visElapsedWeek (43)** <br/> |
| Dias decorridos  <br/> | dd  <br/> |**visElapsedDay (44)** <br/> |
| Horas decorridas  <br/> | hd  <br/> |**visElapsedHour (45)** <br/> |
| Minutos decorridos  <br/> | md  <br/> |**visElapsedMin (46)** <br/> |
| Segundos decorridos  <br/> | sd  <br/> |**Defaultdurationunitsviselapsedsec (47)** <br/> |
| Pés  <br/> | pé  <br/> |**visFeet (66)** <br/> |
| Polegadas  <br/> | pol  <br/> |**visInches (65)** <br/> |
| Quilômetros  <br/> | km  <br/> |**visKilometers (72)** <br/> |
| Metros  <br/> | m  <br/> |**visMeters (71)** <br/> |
| Milhas  <br/> | mi  <br/> |**visMiles (68)** <br/> |
| Milímetros  <br/> | mm  <br/> |**visMillimeters (70)** <br/> |
| Minutos  <br/> | '  <br/> |**visMin (84)** <br/> |
| Milhas náuticas  <br/> | mn  <br/> |**visNautMiles (76)** <br/> |
| Porcentagem  <br/> | %  <br/> |**visPercent (33)** <br/> |
| Paicas  <br/> | p  <br/> |**visPicas (51)** <br/> |
| Pontos  <br/> | pt  <br/> |**visPoints (50)** <br/> |
| Radianos  <br/> | rad  <br/> |**visRadians (83)** <br/> |
| Segundos  <br/> | "  <br/> |**visSec (85)** <br/> |
| Jardas  <br/> | jd  <br/> |**visYards (75)** <br/> |
   
## <a name="compound-units-of-measure"></a>Unidades de medida compostas

Em fórmulas, você pode expressar unidades de medida para os números de compostos usando as abreviações na tabela a seguir. Visio simplifica os resultados e exibe-os nas unidades compostas.
  
Por exemplo, se você digitar 45,635 °, o Visio exibirá o valor equivalente como 45° 38' 6".
  
|**Para especificar unidades**|**Use essa abreviação**|**Constante de automação**|
|:-----|:-----|:-----|
| Cíceros e didots  <br/> | CÍCERO/DIDOT  <br/> |**visCicerosAndDidots (52)** <br/> |
| Graus, minutos e segundos  <br/> | °  <br/> |**visDegreeMinSec (82)** <br/> |
| Pés e polegadas  <br/> | PÉS/POLEGADAS  <br/> |**visFeetAndInches (67)** <br/> |
| Paicas e pontos  <br/> | PAICAPONTOS  <br/> |**visPicasAndPoints (49)** <br/> |
   
## <a name="fractional-units-of-measure"></a>Unidades de medida fracionadas

Você pode especificar unidades fracionais de medida na célula **DrawingScale** afete o número de subdivisões da régua que o Visio exibe na janela de desenho. Por padrão, o Visio divide a distâncias em décimos quando seus réguas de desenho. Se você usar unidades fracionais de medida na célula **DrawingScale** , o Visio divide a distância no seguinte: 
  
- Oitavos para *visInchFrac* e *visMileFrac* 
    
- Duodécimos para *visFeetAndInches* 
    
As unidades de medida fracionadas só afetam a célula DrawingScale
  
|**Para especificar unidades fracionais**|**Use essa abreviação**|**Constante de automação**|
|:-----|:-----|:-----|
| Polegadas em frações  <br/> | IN_F  <br/> |**visInchFrac (73)** <br/> |
| Milhas em frações  <br/> | MI_F  <br/> |**visMileFrac (74)** <br/> |
| Pés e polegadas  <br/> | PÉS/POLEGADAS  <br/> |**visFeetAndInches (67)** <br/> |
   
## <a name="multidimensional-units-of-measure"></a>Unidades de medida multidimensionais

Em fórmulas, você pode expressar unidades de medida para números multidimensionais usando as abreviações da tabela a seguir. O Visio simplifica os resultados e os exibe nas unidades multidimensionais.
  
|**Para especificar unidades multidimensionais**|**Use essa abreviação**|**Constante de automação**|
|:-----|:-----|:-----|
| Acre  <br/> | ACRES  <br/> |**visAcre (36)** <br/> |
| Centímetros  <br/> | SQ. CM., SQ CM, CM.^2, CM^2  <br/> |**visCentimeters (69)** <br/> |
| Pés  <br/> | SQ. FT., SQ FT, FT.^2, FT^2  <br/> |**visFeet (66)** <br/> |
| Hectare  <br/> | HECTARES, HECTARE, HA., HA  <br/> |**visHectare (37)** <br/> |
| Polegadas  <br/> | SQ. IN., SQ IN, IN.^2, IN^2  <br/> |**visInches (65)** <br/> |
| Quilômetros  <br/> | SQ. KM., SQ KM, KM.^2, KM ^2  <br/> |**visKilometers (72)** <br/> |
| Metros  <br/> | SQ. M., SQ M, M.^2, M ^2  <br/> |**visMeters (71)** <br/> |
| Milhas  <br/> | SQ. MI., SQ MI, MI.^2, MI ^2  <br/> |**visMiles (68)** <br/> |
| Milímetros  <br/> | SQ. MM., SQ MM, MM.^2, MM ^2  <br/> |**visMillimeters (70)** <br/> |
| Jardas  <br/> | SQ. YD., SQ YD, YD.^2, YD^2  <br/> |**visYards (75)** <br/> |
   
## <a name="universal-strings"></a>Cadeias de caracteres universais

Em versões localizadas do Visio, o conjunto de cadeias de caracteres reconhecidas muda com o idioma. Se quiser que seu programa trabalhe com vários idiomas, use as cadeias de caracteres universais como unidades de medida.
  
|**Para**|**Uso**|
|:-----|:-----|
| Centímetros  <br/> | CM  <br/> |
| Cíceros  <br/> | C  <br/> |
| Cíceros e didots  <br/> | CÍCERO/DIDOT  <br/> |
| Data ou hora  <br/> | DATA  <br/> |
| Graus  <br/> | GRA  <br/> |
| Graus, minutos e segundos  <br/> | °  <br/> |
| Didots  <br/> | D  <br/> |
| Semana decorrida  <br/> | SD  <br/> |
| Dia decorrido  <br/> | DD  <br/> |
| Hora decorrida  <br/> | HD  <br/> |
| Minuto decorrido  <br/> | MD  <br/> |
| Segundo decorrido  <br/> | SD  <br/> |
| Pés  <br/> | PÉ  <br/> |
| Pés e polegadas  <br/> | PÉS/POLEGADAS  <br/> |
| Polegadas  <br/> | POL  <br/> |
| Polegadas em frações  <br/> | IN_F  <br/> |
| Quilômetros  <br/> | KM  <br/> |
| Metros  <br/> | M  <br/> |
| Milhas  <br/> | MI  <br/> |
| Milhas em frações  <br/> | MI_F  <br/> |
| Milímetros  <br/> | MM  <br/> |
| Minutos  <br/> | '  <br/> |
| Milhas náuticas  <br/> | MN  <br/> |
| Por cento  <br/> | %  <br/> |
| Paicas  <br/> | P  <br/> |
| Paicas e pontos  <br/> | PAICAPONTOS  <br/> |
| Pontos  <br/> | PT  <br/> |
| Radianos  <br/> | RAD  <br/> |
| Segundos  <br/> | "  <br/> |
| Jardas  <br/> | JD  <br/> |
   
## <a name="implicit-units-of-measure"></a>Unidades implícitas de medida

Quando o Visio analisa e armazena um par número-unidade, pode usar unidades explícitas ou unidades implícitas. Um número expresso em unidades explícitas sempre é exibido nas unidades de medida originalmente inseridas. Um número expresso em unidades implícitas sempre será convertido no valor equivalente de unidades de desenho, de página ou angulares adequados à célula.
  
Por exemplo, suponha que você insira o equivalente a 1 polegada na célula A usando unidades explícitas e na célula B usando unidades implícitas, e que tanto a célula A como a célula B usem unidades de desenho. Em seguida, você altera as unidades padrão da página para centímetros. A célula A ainda exibirá 1 pol., já que usa unidades explícitas que não são alteradas com os padrões. A célula B agora exibe 2,54 cm, o valor equivalente nas unidades padrão.
  
Para inserir unidades implicitamente, use a sintaxe a seguir.
  
```vb
number  [unit , flag ]
```

|||
|:-----|:-----|
| _number_ <br/> |O valor original, como 3,7, 1,7E-4 ou 5 1/2.  <br/> |
| _unidade_ <br/> |As unidades nas quais _número_ originalmente é expresso.  <br/> |
| _sinalizador_ <br/> |O sistema de medidas a ser usado quando a unidade de valor implícito for exibida. Consulte abaixo para obter os valores.  <br/> |
   
O parâmetro _sinalizador_ é uma das seguintes letras (maiusculas ou minúsculas) indicando o sistema de medida que deve ser usado quando a unidade de valor implícito é exibida. 
  
|**_Sinalizador_**|**Sistema de medida**|**Exemplo**|
|:-----|:-----|:-----|
| a, A  <br/> | Angular  <br/> | =5[grau,A]  <br/> |
| d, D  <br/> | Desenho  <br/> | =5[pol,D]  <br/> |
| e, E  <br/> | Duração  <br/> | =5[hd,E]  <br/> |
| p, P  <br/> | Página  <br/> | =5[pol,P]  <br/> |
| t, T  <br/> | Tipo  <br/> | =5[pt,T]  <br/> |
   
Além disso, você pode usar as unidades implícitas DL, DP, DT, DA, DE para desenho - implícita, página-, texto-, angulares-e unidades de tempo, respectivamente. Essas unidades pressupõem que o valor associado é unidades internas. Por exemplo, se o sistema de medida atual for centímetros, *= 2 DL* seria ser interpretada como 2 unidades internas (polegadas) e exibido como 5,08 cm. 
  
Usando a sintaxe implícita descrita acima, essa expressão (=2 DL) é equivalente a 2[in,d]. A sintaxe implícita oferece a opção de interpretação do valor e, portanto, você também poderia especificar 2[ft,d], o que seria interpretado como 2 pés e exibido como 60,96 cm. As unidades implícitas DL, DP, DT, DA e DE são universais e não têm contrapartes localizadas.
  
## <a name="default-units-of-measure"></a>Unidades de medida padrão

A seguir, as unidades de medida padrão junto com as configurações equivalentes na interface do usuário.
  
|**Unidade de medida padrão**|**Interface do usuário equivalente**|
|:-----|:-----|
|**visDrawingUnits** <br/> |As unidades na célula DrawingScale da página ou mestre que contém a célula.  <br/> |
|**visPageUnits** <br/> |As unidades selecionadas na caixa **unidades de medida** na guia **Propriedades da página** da caixa de diálogo **Configurar página** (na guia **Design** , clique na seta **Configurar página** ).  <br/> |
|**visTypeUnits** <br/> |As unidades selecionadas na caixa de **texto** em **Exibir** na guia **Avançado** da caixa de diálogo **Opções do Visio** (clique na guia **arquivo** e, em seguida, clique em **Opções**).  <br/> |
|**visAngleUnits** <br/> |As unidades selecionadas na caixa **ângulo** em **Exibir** na guia **Avançado** da caixa de diálogo **Opções do Visio** .  <br/> |
|**visDurationUnits** <br/> |As unidades selecionadas na caixa **duração** em **Exibir** na guia **Avançado** da caixa de diálogo **Opções do Visio** .  <br/> |
   

