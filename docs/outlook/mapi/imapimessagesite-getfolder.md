---
title: IMAPIMessageSiteGetFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetFolder
api_type:
- COM
ms.assetid: 9f4b4147-ed98-47cb-a799-ddf028f8e826
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: ea95ea4efbbf50e5551a27eb81fe5d5ab3b73948
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767071"
---
# <a name="imapimessagesitegetfolder"></a>IMAPIMessageSite::GetFolder

  
  
**Aplica-se a**: Outlook 
  
Retorna a pasta na qual a mensagem atual foi criada ou aberta, se existir uma pasta tal. Este método retornará NULL no parâmetro _ppFolder_ mensagens incorporado, o que não são armazenadas diretamente em uma pasta. 
  
```cpp
HRESULT GetFolder(
  LPMAPIFOLDER FAR * ppFolder
);
```

## <a name="parameters"></a>Par�metros

 _ppFolder_
  
> [out] Um ponteiro para um ponteiro para a pasta retornado.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
S_FALSE 
  
> Nenhuma pasta existe para a mensagem.
    
## <a name="remarks"></a>Coment�rios

Para obter uma lista das interfaces que estão relacionados aos servidores de formulário, consulte [Interfaces de formulário de MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetFolder  <br/> |MFCMAPI usa o método **IMAPIMessageSite::GetFolder** para retornar o ponteiro atualmente em cache para a pasta especificada.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulário MAPI](mapi-form-interfaces.md)

