---
title: OR (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7190523-87cf-4e04-aef4-d229776cd16b
description: Combina duas condições. Retorna VERDADEIRO quando uma das duas condições for verdadeira.
ms.openlocfilehash: ffa605d2403c5aa8396d89f78d0bb7dd11343540
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414757"
---
# <a name="or-access-custom-web-app"></a>OR (aplicativo Web personalizado do Access)

Combina duas condições. Retorna VERDADEIRO quando uma das duas condições for verdadeira.
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

 *BooleanExpression* **ou** *BooleanExpression* 
  
O **operador Or** usa o argumento a seguir. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *BooleanExpression*  <br/> |Qualquer expressão válida que retorne VERDADEIRO ou FALSO.  <br/> |
   
## <a name="remarks"></a>Comentários

Quando mais de um operador lógico é usado em uma instrução, **os operadores Or** são avaliados após **operadores And.** No entanto, você pode alterar a ordem de avaliação usando parênteses. 
  
A tabela a seguir mostra o resultado do operador **Or.** 
  
||**TRUE**|**FALSE**|
|:-----|:-----|:-----|
|**TRUE** <br/> |TRUE  <br/> |TRUE  <br/> |
|**FALSE** <br/> |TRUE  <br/> |FALSE  <br/> |
   

