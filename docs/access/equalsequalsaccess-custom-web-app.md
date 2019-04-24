---
title: Equals (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70bc707a-3a61-4d75-816d-0defd0806319
description: Compara a igualdade de duas expressões.
ms.openlocfilehash: 8c551e3dbc057433b49bc2558e08feba5ee3d04f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308222"
---
# <a name="equals-access-custom-web-app"></a>Equals (aplicativo Web personalizado do Access)

Compara a igualdade de duas expressões.
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

`= (Equals)`

**  =  *expressão* de expressão 
  
*expression* Trata-se de qualquer expressão válida. Se as expressões não forem do mesmo tipo de dados, o tipo de dados de uma expressão deverá ser implicitamente conversível no tipo de dados da outra. A conversão depende das regras de precedência do tipo de dados. 
  
## <a name="return-type"></a>Tipo de retorno

**Boolean**
  
## <a name="remarks"></a>Comentários

Quando você compara duas expressões nulas, o resultado é TRUE.
  
Comparar NULL com um valor não nulo sempre resulta em FALSE.
  

