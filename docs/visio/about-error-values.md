---
title: Sobre valores de erro
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251832
localization_priority: Normal
ms.assetid: 56430658-a798-c004-b4ba-363443f43ded
description: Os valores de erro são exibidos em células que contêm fórmulas incorretas para essa célula.
ms.openlocfilehash: 5219becdd1af888e424a2fe33faa7df5a06f61fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332603"
---
# <a name="about-error-values"></a>Sobre valores de erro

Os valores de erro são exibidos em células que contêm fórmulas incorretas para essa célula.
  
Se uma fórmula fizer referência a uma célula que contenha um valor de erro, essa fórmula também exibirá um valor de erro. Use as funções ISERR, ISERRNA, ISERROR ou ISERRVALUE para procurar valores de erro.
  
**Valores de erro**

||||
|:-----|:-----|:-----|
|**Se a célula exibir** <br/> |**A fórmula inclui** <br/> |**Exemplo** <br/> |
| #DIV/0!  <br/> |Divisão por 0  <br/> |10/0  <br/> |
| #VALUE!  <br/> | Um argumento ou operando do tipo errado  <br/> | 5 + "House"  <br/> |
| #REF!  <br/> | Uma referência a uma célula que não existe  <br/> | Uma célula que faz referência a uma outra célula que não existe mais  <br/> |
| #NUM!  <br/> | Um número inválido  <br/> | Raiz quadrada de um número negativo  <br/> |
| #N/A!  <br/> | Não é um valor disponível  <br/> | Função NA( )  <br/> |
| #DIM!  <br/> | Um valor dimensional que excede o intervalo de dimensão (as potências válidas são \<números inteiros \<-128 = n = 127)  <br/> Um valor dimensional usado com uma operação inadequada  <br/> |1in ^ 100 \* 1in ^ 100 (o resultado é 1in ^ 200, que está além do intervalo de dimensão)  <br/> 5,2cm^1,5 (não é uma potência inteira)  <br/> |
   

