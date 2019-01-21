---
title: IS [NOT] NULL (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: b941a0c7-9753-4920-bb6d-cbba94ba9422
description: Determina se a expressão especificada é NULL.
localization_priority: Priority
ms.openlocfilehash: fe6a0fe4f182a1385304b783e7cfaaf515f732d4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699312"
---
# <a name="is-not-null-access-custom-web-app"></a>IS [NOT] NULL (aplicativo Web personalizado do Access)

Determina se a expressão especificada é NULL.
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/pt-BR/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

 *expression* **IS** [*NOT*] **NULL**
  
O predicado **IS [NOT] NULL** contém os seguintes argumentos. 
  
|||
|:-----|:-----|
| *expression*  <br/> |Qualquer expressão válida.  <br/> |
| *NOT*  <br/> |Especifica se o resultado booliano pode ser negado. O predicado inverte os respectivos valores de retorno, retornando TRUE se o valor não for NULL e FALSE se o valor for NULL.  <br/> |
   
## <a name="remarks"></a>Comentários

Se o valor de *expression* for NULL, então IS NULL retornará TRUE. Caso contrário, retornará FALSE. 
  
Se o valor de expression for NULL, então IS NOT NULL retornará FALSE. Caso contrário, retornará TRUE.
  

