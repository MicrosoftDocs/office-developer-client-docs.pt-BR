---
title: '[Não] é NULL (aplicativo da web personalizado do Access)'
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b941a0c7-9753-4920-bb6d-cbba94ba9422
description: Determina se a expressão especificada é NULL.
ms.openlocfilehash: fcbceb1e8edac65fe232ba9c2b12195b99db9545
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765075"
---
# <a name="is-not-null-access-custom-web-app"></a>[Não] é NULL (aplicativo da web personalizado do Access)

Determina se a expressão especificada é NULL.
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

 *expressão* **Encontra** [ *Não* ] **Nulo**
  
O **IS [NOT] NULL** predicado contém os seguintes argumentos. 
  
|||
|:-----|:-----|
| *expressão*  <br/> |Qualquer expressão válida.  <br/> |
| *NOT*  <br/> |Especifica que o resultado booleano ser negadas. O predicado reverte seus valores de retorno, retornando TRUE se o valor não for NULL e FALSE se o valor é nulo.  <br/> |
   
## <a name="remarks"></a>Comentários

Se o valor da *expressão* for NULL, é nulo retorna TRUE; Caso contrário, ele retornará FALSE. 
  
Se o valor da expressão for NULL, não é NULL retorna FALSE; Caso contrário, ele retornará TRUE.
  

