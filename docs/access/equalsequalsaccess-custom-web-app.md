---
title: É igual a (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70bc707a-3a61-4d75-816d-0defd0806319
description: Compara a igualdade de duas expressões.
ms.openlocfilehash: efdd06a1735190d63c13c4df8230e1d29d71c1dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765085"
---
# <a name="equals-access-custom-web-app"></a>É igual a (aplicativo da web personalizado do Access)

Compara a igualdade de duas expressões.
  
> [!IMPORTANT]
> [!IMPORTANTE] A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Syntax

`= (Equals)`

*expressão*  =  *expressão* 
  
*expressão*  É qualquer expressão válida. Se as expressões não são do mesmo tipo de dados, o tipo de dados para uma expressão deve ser implicitamente conversível ao tipo de dados do outro. A conversão depende as regras de precedência de tipo de dados. 
  
## <a name="return-type"></a>Tipo de retorno

**Boolean**
  
## <a name="remarks"></a>Comentários

Quando você compara duas expressões nulo, o resultado é TRUE.
  
Comparar NULL como um valor não-nulo sempre resulta em FALSE.
  

