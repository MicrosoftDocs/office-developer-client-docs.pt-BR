---
title: Usando macros para tratamento de erros
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9e6901d6583e7a7924a4a7c19c0a262bcef74bd3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435562"
---
# <a name="using-macros-for-error-handling"></a>Usando macros para tratamento de erros

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Há várias macros para facilitar o trabalho com valores HRESULT.
  
Há dois conjuntos de macros que testam se há falha ou sucesso: HR_SUCCEEDED e HR_FAILED êxito e FALHA. SUCCEEDED é o mesmo que HR_SUCCEEDED e FAILED é o mesmo que HR_FAILED.
  
Nesse caso, use a macro **ResultFromScode** para definir a variável HRESULT com o valor HRESULT correspondente para S_OK. 
  
As macros comumente usadas são brevemente descritas na tabela a seguir.
  
|**Macro**|**Descrição**|
|:-----|:-----|
|**MAKE_HRESULT** <br/> |Constrói um HRESULT a partir de seus componentes.  <br/> |
|**HR_SUCCEEDED** <br/> |Testa um HRESULT para uma condição de sucesso ou aviso.  <br/> |
|**HR_FAILED** <br/> |Testa um HRESULT para uma condição de erro.  <br/> |
|**HRESULT_CODE** <br/> |Extrai a parte do código de erro do HRESULT.  <br/> |
|**HRESULT_FACILITY** <br/> |Extrai as instalações do HRESULT.  <br/> |
|**HRESULT_SEVERITY** <br/> |Extrai o bit de severidade da SEVERITY.  <br/> |
|**SUCCEEDED** <br/> |Testa um HRESULT para uma condição de sucesso ou aviso.  <br/> |
|**FALHA** <br/> |Testa um HRESULT para uma condição de erro.  <br/> |
   

