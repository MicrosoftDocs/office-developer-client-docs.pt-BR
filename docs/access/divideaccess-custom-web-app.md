---
title: /(Divisão) (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3d296730-197b-44db-853b-881597dd9b48
description: Divide um número por outro.
ms.openlocfilehash: 48d43b224743949f86c5d206d9919a9e2d6fbcae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308257"
---
# <a name="-divide-access-custom-web-app"></a>/(Divisão) (aplicativo Web personalizado do Access)

Divide um número por outro.
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

 **  /  *divisor* de dividendo 
  
 *dividendo*  É a expressão numérica a ser dividida. Pode ser qualquer expressão válida de qualquer um dos tipos de dados da categoria de tipo de dados numéricos, exceto o tipo de dados DateTime. 
  
 *Divisor*  É a expressão numérica pela qual dividir o dividendo. Pode ser qualquer expressão válida de qualquer um dos tipos de dados da categoria de tipo de dados numéricos, exceto o tipo de dados DateTime. 
  
## <a name="return-type"></a>Tipo de retorno

Retorna o tipo de dados do argumento com maior precedência. 
  
Se um *dividendo* inteiro for dividido por um *divisor* inteiro, o resultado será um inteiro que tenha qualquer parte fracionária do resultado truncado. 
  
## <a name="remarks"></a>Comentários

O valor real retornado pelo operador/é o quociente da primeira expressão dividida pela segunda expressão.
  

