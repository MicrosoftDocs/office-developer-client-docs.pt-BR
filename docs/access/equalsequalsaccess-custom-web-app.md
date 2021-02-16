---
title: Equals(Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70bc707a-3a61-4d75-816d-0defd0806319
description: Compara a igualdade de duas expressões.
ms.openlocfilehash: 8c551e3dbc057433b49bc2558e08feba5ee3d04f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408926"
---
# <a name="equals-access-custom-web-app"></a>Igual a (aplicativo Web personalizado do Access)

Compara a igualdade de duas expressões.
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

`= (Equals)`

*expressão*   =   *expressão* 
  
*expression* Trata-se de qualquer expressão válida. Se as expressões não são do mesmo tipo de dados, o tipo de dados de uma expressão deve ser implicitamente conversível para o tipo de dados da outra. A conversão depende das regras de precedência do tipo de dados. 
  
## <a name="return-type"></a>Tipo de retorno

**Boolean**
  
## <a name="remarks"></a>Comentários

Quando você compara duas expressões NULL, o resultado é VERDADEIRO.
  
Comparar NULL a um valor não NULO sempre resulta em FALSE.
  

