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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329652"
---
# <a name="using-macros-for-error-handling"></a>Usando macros para tratamento de erros

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Há várias macros para facilitar o trabalho com valores HRESULT.
  
Há dois conjuntos de macros que testam a falha ou o êxito: HR_SUCCEEDED e HR_FAILED e com êxito e falha. SUCCEEDed é o mesmo que HR_SUCCEEDED e FAILED é o mesmo que HR_FAILED.
  
Nesse caso, use a macro **ResultFromScode** para definir a variável HRESULT para o valor HRESULT correspondente de S_OK. 
  
As macros comumente usadas são descritas brevemente na tabela a seguir.
  
|**Macro**|**Descrição**|
|:-----|:-----|
|**MAKE_HRESULT** <br/> |Constrói um HRESULT a partir de seus componentes.  <br/> |
|**HR_SUCCEEDED** <br/> |Testa um HRESULT para uma condição de êxito ou de aviso.  <br/> |
|**HR_FAILED** <br/> |Testa um HRESULT para uma condição de erro.  <br/> |
|**HRESULT_CODE** <br/> |Extrai a parte do código de erro do HRESULT.  <br/> |
|**HRESULT_FACILITY** <br/> |Extrai o recurso do HRESULT.  <br/> |
|**HRESULT_SEVERITY** <br/> |Extrai o bit de severidade da severidade.  <br/> |
|**ADICIONADA** <br/> |Testa um HRESULT para uma condição de êxito ou de aviso.  <br/> |
|**FALHOU** <br/> |Testa um HRESULT para uma condição de erro.  <br/> |
   

