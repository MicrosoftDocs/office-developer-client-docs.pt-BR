---
title: Função Round (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4af7fbe2-ee34-4a52-b55e-ce3983313b5e
description: Retorna um valor numérico, arredondado ou truncado, para o comprimento ou precisão especificado.
ms.openlocfilehash: 5a3df4a4ddd7aace5edf886db5988704e5dd6af3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765227"
---
# <a name="round-function-access-custom-web-app"></a>Função Round (aplicativo Web personalizado do Access)

Retorna um valor numérico, arredondado ou truncado, para o comprimento ou precisão especificado.
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/pt-BR/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

 **Round** (*Número*, *Precisão*, [*TruncateInsteadOfRound*]) 
  
A função **Round** contém os argumentos a seguir. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *Número*  <br/> |Uma expressão numérica  <br/> |
| *Precisão*  <br/> |A precisão com a qual o  *Número*  deve ser arredondado.  *Precisão*  deve ser uma expressão numérica. Quando  *Precisão*  for um número positivo,  *Número*  será arredondado para o número de posições decimais especificados por comprimento. Quando  *Precisão*  for um número negativo,  *Número*  será arredondado no lado esquerdo da vírgula decimal, como especificado por comprimento.  <br/> |
| *TruncateInsteadOfRound*  <br/> |O tipo de operação a ser executada. Quando omitido ou definido como 0,  *Número*  será arredondado. Quando um valor diferente de 0 for especificado,  *Número*  será truncado. O valor padrão é 0.  <br/> |
   
## <a name="remarks"></a>Comentários

 **Round** sempre retorna um valor. Se o comprimento for negativo e maior do que o número de dígitos anteriores à vírgula decimal, **Round** retornará 0. 
  

