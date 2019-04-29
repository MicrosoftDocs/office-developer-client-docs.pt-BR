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
ms.openlocfilehash: d80c73aef780a0da39f3939f71462488a067de5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432944"
---
# <a name="removepreprocessinfo"></a>RemovePreprocessInfo

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Remove informações preprocessadas gravadas por uma função baseada em [PreprocessMessage](preprocessmessage.md) de uma mensagem. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapispi. h  <br/> |
|Função definida implementada por:  <br/> |Provedores de transporte  <br/> |
|Função definida chamada por:  <br/> |Spooler MAPI  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a>Parâmetros

 _lpMessage_
  
> no Ponteiro para a mensagem pré processada da qual as informações serão removidas.
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> As informações preprocessadas foram removidas com êxito.
    
## <a name="remarks"></a>Comentários

O spooler MAPI chama uma função com base no **RemovePreprocessInfo**. Um provedor de transporte registra a função baseada em **RemovePreprocessInfo** ao mesmo tempo em que registra a função do **PreprocessMessage** em paralelo em uma chamada para o método [IMAPISupport:: RegisterPreprocessor](imapisupport-registerpreprocessor.md) . 
  
Uma renderização de imagem adequada para transmissão de fax é um exemplo de informações preprocessadas gravadas por uma função definida pelo protótipo de função [PreprocessMessage](preprocessmessage.md). O spooler MAPI normalmente chama uma função **RemovePreprocessInfo** após enviar uma mensagem que contém informações preprocessadas. 
  

