---
title: OU (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7190523-87cf-4e04-aef4-d229776cd16b
description: Combina duas condições. Retorna TRUE quando uma das duas condições for verdadeira.
ms.openlocfilehash: 8ccf4a12644f45e80756f72013d42310fece07fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765199"
---
# <a name="or-access-custom-web-app"></a>OU (aplicativo da web personalizado do Access)

Combina duas condições. Retorna TRUE quando uma das duas condições for verdadeira.
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

 *BooleanExpression* **Ou** *BooleanExpression* 
  
O operador **Or** utiliza o argumento a seguir. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *BooleanExpression*  <br/> |Qualquer expressão válida que retorna TRUE ou FALSE.  <br/> |
   
## <a name="remarks"></a>Comentários

Quando mais de um operador lógico é usado em uma instrução, **ou** operadores são avaliadas após **e** operadores. No entanto, você pode alterar a ordem de avaliação usando parênteses. 
  
A tabela a seguir mostra o resultado do operador **ou** . 
  
||**TRUE**|**FALSE**|
|:-----|:-----|:-----|
|**TRUE** <br/> |VERDADEIRO  <br/> |VERDADEIRO  <br/> |
|**FALSE** <br/> |VERDADEIRO  <br/> |FALSO  <br/> |
   

