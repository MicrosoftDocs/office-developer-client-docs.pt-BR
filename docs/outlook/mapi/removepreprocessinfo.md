---
title: RemovePreprocessInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.RemovePreprocessInfo
api_type:
- COM
ms.assetid: 25f46937-abac-4a0b-83db-eeac9451c112
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fab8860621cee5a87b087ee9d98f373baa278e45
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770264"
---
# <a name="removepreprocessinfo"></a>RemovePreprocessInfo

  
  
**Aplica-se a**: Outlook 
  
Remove preprocessada informações escritas por uma função [PreprocessMessage](preprocessmessage.md) com base em uma mensagem. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapispi.h  <br/> |
|Função definido implementada por:  <br/> |Provedores de transporte  <br/> |
|Função definido chamada pelo:  <br/> |Spooler MAPI  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a>Parâmetros

 _lpMessage_
  
> [in] Ponteiro para a mensagem pré-processado do qual as informações são a ser removido.
    
## <a name="return-value"></a>Valor retornado

S_OK
  
> Informações pré-processado foi removidas com êxito.
    
## <a name="remarks"></a>Comentários

O MAPI spooler chama uma função com base em **RemovePreprocessInfo**. Um provedor de transporte registra a função **RemovePreprocessInfo** com base ao mesmo tempo em que ele registra a função de **PreprocessMessage** com base em paralelo em uma chamada ao método [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) . 
  
Uma imagem de renderização adequado para a transmissão de fax é um exemplo de informação pré-processado escrito por uma função definida pelo protótipo de função [PreprocessMessage](preprocessmessage.md). O MAPI spooler geralmente chama uma função de **RemovePreprocessInfo** após enviar uma mensagem que contém informações pré-processado. 
  

