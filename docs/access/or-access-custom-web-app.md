---
title: OU (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7190523-87cf-4e04-aef4-d229776cd16b
description: Combina duas condições. Retorna TRUE quando uma das duas condições é true.
ms.openlocfilehash: ffa605d2403c5aa8396d89f78d0bb7dd11343540
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308068"
---
# <a name="or-access-custom-web-app"></a>OU (aplicativo Web personalizado do Access)

Combina duas condições. Retorna TRUE quando uma das duas condições é true.
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

 *Valor booleano* **Ou** *Valor booleano* 
  
O operador **or** usa o argumento a seguir. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *Valor booleano*  <br/> |Qualquer expressão válida que retorne TRUE ou FALSE.  <br/> |
   
## <a name="remarks"></a>Comentários

Quando mais de um operador lógico é usado em uma instrução, **ou** os operadores são avaliados depois **de operadores e** . No enTanto, você pode alterar a ordem de avaliação usando parênteses. 
  
A tabela a seguir mostra o resultado do operador **or** . 
  
||**VERDADEIRO**|**FALSE**|
|:-----|:-----|:-----|
|**VERDADEIRO** <br/> |TRUE  <br/> |TRUE  <br/> |
|**FALSE** <br/> |TRUE  <br/> |FALSE  <br/> |
   

