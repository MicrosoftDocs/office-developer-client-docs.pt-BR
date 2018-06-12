---
title: ENTRE (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: Especifica um intervalo a ser testado.
ms.openlocfilehash: 0ef3384d6a29826968220f8d6cfc0d2f85e1131c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765072"
---
# <a name="between-access-custom-web-app"></a>ENTRE (aplicativo da web personalizado do Access)

Especifica um intervalo a ser testado.
  
> [!IMPORTANT]
> [!IMPORTANTE] A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Syntax

 *test_expression*  [NOT] **BETWEEN** *begin_expression* **AND** *end_expression* 
  
O operador **entre** contém os seguintes argumentos. 
  
|**Argumento**|**Obrigatório**|**Descrição**|
|:-----|:-----|:-----|
| *test_expression*  <br/> |Sim  <br/> |A expressão para testar os no intervalo definido por *begin_expression* e *end_expression* . Deve ser do mesmo tipo de dados que *begin_expression* e o *end_expression* .  <br/> |
| *NOT*  <br/> |Não  <br/> |Especifica que o resultado do predicado ser negadas.  <br/> |
| *begin_expression*  <br/> |Sim  <br/> |Uma expressão válida. Deve ser do mesmo tipo de dados que *test_expression* e o *end_expression* .  <br/> |
| *end_expression*  <br/> |Sim  <br/> |Uma expressão válida. Deve ser do mesmo tipo de dados que *test_expression* e o *begin_expression* .  <br/> |
| *AND*  <br/> |Sim  <br/> |Indica a *test_expression* deve estar dentro do intervalo indicado pela *begin_expression* e *end_expression* .  <br/> |
   
## <a name="result-type"></a>Tipo de resultado

 **Boolean**
  
## <a name="remarks"></a>Comentários

 **BETWEEN** retorna **TRUE** se o valor de *test_expression* for maior que ou igual ao valor de *begin_expression* e menor ou igual ao valor de *end_expression* . 
  
 **Não entre** retorna **TRUE** se o valor de *test_expression* for menor que o valor de *begin_expression* ou maior que o valor da *end_expression* . 
  
Para especificar um intervalo exclusivo, use o maior que (\>) e menor que operadores (\<).
  

