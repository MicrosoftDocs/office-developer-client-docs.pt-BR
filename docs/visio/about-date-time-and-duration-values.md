---
title: Sobre valores de data, hora, duração
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251852
localization_priority: Normal
ms.assetid: b6951a92-f32a-5829-5e07-b277b7934df3
description: É possível executar operações em fórmulas usando valores de data, hora e duração. No Microsoft Visio, uma expressão de data e tempo pode ser avaliada como um único valor. Uma expressão de data e hora é qualquer expressão comumente reconhecida como uma data e/ou hora ou uma referência a uma célula que contenha uma data e/ou hora. Isso inclui cadeias de caracteres e números que pareçam uma data e hora, e valores de data e hora retornados de funções.
ms.openlocfilehash: 56de919fa713c0948bb87f794d1c6e0a5d727aef
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416724"
---
# <a name="about-date-time-and-duration-values"></a>Sobre valores de data, hora e duração

É possível executar operações em fórmulas usando valores de data, hora e duração. No Microsoft Visio, uma expressão de data e tempo pode ser avaliada como um único valor. Uma expressão de data e hora é qualquer expressão comumente reconhecida como uma data e/ou hora ou uma referência a uma célula que contenha uma data e/ou hora. Isso inclui cadeias de caracteres e números que pareçam uma data e hora, e valores de data e hora retornados de funções.
  
Valores de data e hora no Visio são armazenados internamente como um número de ponto flutuante de 64 bits. O valor à esquerda do decimal representa o número de dias desde 30 de dezembro de 1899. O valor à direita do decimal representa a fração de um dia desde a meia-noite. O meio-dia é representado por 0,5.
  
Para usar datas e horas dentro de uma expressão (em vez de uma única constante), é necessário usar a função adequada para identificá-las como valores de data e hora.
  
## <a name="valid-dates"></a>Datas válidas

||||
|:-----|:-----|:-----|
| "2/28"  <br/> | "2/28/99"  <br/> | "2/28/1999"  <br/> |
| "2-28"  <br/> | "2-28-99"  <br/> | "2-28/1999"  <br/> |
| "6-mar-99"  <br/> | "6-mar"  <br/> | "6-mar-99"  <br/> |
| "1º de janeiro de 1999"  <br/> | "1º -jan-99"  <br/> | "1º -jan-1999"  <br/> |
| "janeiro de 2000"  <br/> | "janeiro, 2000"  <br/> | "1º -jan-00"  <br/> |
   
## <a name="valid-times"></a>Horas válidas

||||
|:-----|:-----|:-----|
| "3:45"  <br/> | "3:45:27"  <br/> | "7a"  <br/> |
| "7 a.m."  <br/> | "7 p."  <br/> | "7h30 p.m."  <br/> |
   
## <a name="date-and-time-functions"></a>Funções de data e hora

|**Function**|**Description**|
|:-----|:-----|
|[PÓS-DATADOS](date-function-visioshapesheet.md) <br/> | Converte números em um valor de data.  <br/> |
|[DATETIME](datetime-function.md) <br/> | Converte uma sequência de caracteres em um valor de data e hora.  <br/> |
|[Date](datevalue-function-visioshapesheet.md) <br/> | Converte uma sequência de caracteres em um valor de data.  <br/> |
|[AGORA](now-function-visioshapesheet.md) <br/> | Retorna a data atual do sistema como um valor de data e hora.  <br/> |
|[TEMPORAIS](time-function-visioshapesheet.md) <br/> | Converte números em um valor de hora.  <br/> |
|[TIMEVALUE](timevalue-function-visioshapesheet.md) <br/> | Converte uma sequência de caracteres em um valor de hora.  <br/> |
|[DAY](day-function-visioshapesheet.md) <br/> | Retorna o componente do dia como uma expressão de data e hora.  <br/> |
|[DAYOFYEAR](dayofyear-function.md) <br/> | Retorna o dia do ano sequencial como uma expressão de data e hora.  <br/> |
|[HOUR](hour-function-visioshapesheet.md) <br/> | Retorna o componente de horas como uma expressão de data e hora.  <br/> |
|[MINUTE](minute-function-visioshapesheet.md) <br/> | Retorna o componente de minutos como uma expressão de data e hora.  <br/> |
|[MONTH](month-function-visioshapesheet.md) <br/> | Retorna o componente de mês como uma expressão de data e hora.  <br/> |
|[SECOND](second-function-visioshapesheet.md) <br/> | Retorna o componente de segundos como uma expressão de data e hora.  <br/> |
|[WEEKDAY](weekday-function-visioshapesheet.md) <br/> | Retorna o número do dia da semana como uma expressão de data e hora.  <br/> |
|[YEAR](year-function-visioshapesheet.md) <br/> | Retorna o componente de ano como uma expressão de data e hora.  <br/> |
   
## <a name="duration"></a>Duração

É possível executar operações que calculam a duração ou o tempo decorrido. A duração é armazenada internamente como dias e a fração de um dia. Por exemplo, 1 semana decorrida, 7 dias decorridos e 168 horas decorridas são todos armazenados internamente como 7,0, mas são exibidos com as unidades adequadas.
  
O Visio reconhece as unidades de duração na seguinte tabela.
  
|**Unit**|**Abbreviation**|**Abreviação universal**|
|:-----|:-----|:-----|
| dia decorrido  <br/> | diad, dd.  <br/> | Ed  <br/> |
| hora decorrida  <br/> | horad, hd.  <br/> | HD  <br/> |
| minuto decorrido  <br/> | minutod, md.  <br/> | em  <br/> |
| segundo decorrido  <br/> | segundod, sd.  <br/> | es  <br/> |
| semana decorrida  <br/> | semanad, sd.  <br/> | ova  <br/> |
   
É possível adicionar uma data e hora a uma duração para calcular uma nova data e hora. Você pode executar as operações listadas nessa tabela usando datas, horas e durações.
  
|**Input**|**Resultado**|
|:-----|:-----|
| Data-hora +/- duração  <br/> | Valor de data e hora  <br/> |
| Duração +/- data-hora  <br/> | Valor de data e hora  <br/> |
| Duração +/- duração  <br/> | Valor de duração  <br/> |
| Data-hora + data-hora  <br/> | Valor de data e hora  <br/> |
| Data-hora - data-hora  <br/> | Valor de duração  <br/> |
   

