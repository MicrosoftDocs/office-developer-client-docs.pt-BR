---
title: Usar macros para lidar com erros
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c4e216f2204f4ee97d9eeac81f77ce6a82fff3f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770691"
---
# <a name="using-macros-for-error-handling"></a>Usar macros para lidar com erros

  
  
**Aplica-se a**: Outlook 
  
Há várias macros para tornando mais fácil trabalhar com valores HRESULT.
  
Há dois conjuntos de macros que testam a falha ou sucesso: HR_SUCCEEDED e HR_FAILED e SUCCEEDED e FAILED. SUCESSO é que o mesmo que HR_SUCCEEDED e FAILED é o mesmo HR_FAILED.
  
Nesse caso, use a macro **ResultFromScode** para definir a variável HRESULT com o valor HRESULT correspondente para S_OK. 
  
Macros comumente usadas são descritas resumidamente na tabela a seguir.
  
|**Macro**|**Descrição**|
|:-----|:-----|
|**MAKE_HRESULT** <br/> |Constrói um HRESULT de seus componentes.  <br/> |
|**HR_SUCCEEDED** <br/> |Testa um HRESULT para um sucesso ou condição de aviso.  <br/> |
|**HR_FAILED** <br/> |Testa um HRESULT para uma condição de erro.  <br/> |
|**HRESULT_CODE** <br/> |Extrai a parte do código de erro do HRESULT.  <br/> |
|**HRESULT_FACILITY** <br/> |Extrai a facilidade do HRESULT.  <br/> |
|**HRESULT_SEVERITY** <br/> |Extrai estará definido o bit gravidade da GRAVIDADE.  <br/> |
|**FOI BEM-SUCEDIDA** <br/> |Testa um HRESULT para um sucesso ou condição de aviso.  <br/> |
|**FALHA** <br/> |Testa um HRESULT para uma condição de erro.  <br/> |
   

