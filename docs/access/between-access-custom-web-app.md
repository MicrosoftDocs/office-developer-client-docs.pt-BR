---
title: BETWEEN (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: Especifica um intervalo a ser testado.
ms.openlocfilehash: fd67d1163f6a39779e0202b5ca1ba998ba8650a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280733"
---
# <a name="between-access-custom-web-app"></a>BETWEEN (aplicativo Web personalizado do Access)

Especifica um intervalo a ser testado.
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

 *test_expression*  SIDO **Entre** *begin_expression* **E** *end_expression* 
  
O operador **between** contém os seguintes argumentos. 
  
|**Argumento**|**Obrigatório**|**Descrição**|
|:-----|:-----|:-----|
| *test_expression*  <br/> |Sim  <br/> |A expressão a ser testada no intervalo definido por *begin_expression* e *end_expression* . Deve ser o mesmo tipo de dados que *begin_expression* e *end_expression* .  <br/> |
| *NOT*  <br/> |Não  <br/> |Especifica que o resultado do predicado seja negado.  <br/> |
| *begin_expression*  <br/> |Sim  <br/> |Uma expressão válida. Deve ser o mesmo tipo de dados que *test_expression* e *end_expression* .  <br/> |
| *end_expression*  <br/> |Sim  <br/> |Uma expressão válida. Deve ser o mesmo tipo de dados que *test_expression* e *begin_expression* .  <br/> |
| *AND*  <br/> |Sim  <br/> |Indica que *test_expression* deve estar dentro do intervalo indicado por *begin_expression* e *end_expression* .  <br/> |
   
## <a name="result-type"></a>Tipo de resultado

 **Boolean**
  
## <a name="remarks"></a>Comentários

 **Between** retorna **true** se o valor de *test_expression* for maior ou igual ao valor de *begin_expression* e menor ou igual ao valor de *end_expression* . 
  
 **Not between** retorna **true** se o valor de *test_expression* for menor que o valor de *begin_expression* ou maior do que o valor de *end_expression* . 
  
Para especificar um intervalo exclusivo, use os operadores maior que\>() e menor que (\<).
  

