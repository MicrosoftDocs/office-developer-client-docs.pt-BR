---
title: IMSLogonOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.OpenEntry
api_type:
- COM
ms.assetid: 612cbab7-60cb-48bb-906e-18d9135e7a86
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e9d9ca56a877c0106c76242fe97ce43321e62e08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767542"
---
# <a name="imslogonopenentry"></a>IMSLogon::OpenEntry

  
  
**Aplica-se a**: Outlook 
  
Abre uma pasta ou um objeto de mensagem e retorna um ponteiro para o objeto para fornecer mais acesso. 
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulOpenFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Par�metros

 _cbEntryID_
  
> [in] O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Um ponteiro para o endereço do identificador de entrada do objeto folder ou a mensagem para abrir. 
    
 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) para o objeto. Passar NULL indica que o objeto é convertido para a interface padrão para um objeto desse tipo. O parâmetro _lpInterface_ também pode ser definido como um identificador para uma interface apropriada para o objeto. 
    
 _ulOpenFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como o objeto é aberto. Sinalizadores a seguir podem ser definidos:
    
MAPI_BEST_ACCESS 
  
> O objeto deve ser aberto com as permissões máxima permitidas para o usuário e as permissões do aplicativo cliente máximo. Por exemplo, se o cliente tem a permissão de leitura/gravação, o objeto é aberto com permissão de leitura/gravação; Se o cliente tem a permissão somente leitura, o objeto é aberto com permissão somente leitura. O cliente pode recuperar o nível de permissão, fazendo com que a propriedade **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
    
MAPI_DEFERRED_ERRORS 
  
> A chamada será autorizada de sucesso, mesmo se o objeto subjacente não está disponível para o aplicativo de chamada. Se o objeto não estiver disponível, uma chamada subsequente ao objeto pode retornar um erro.
    
MAPI_MODIFY 
  
> Permissão de leitura/gravação solicitações. Por padrão, são criados objetos com permissão somente leitura e os clientes não devem funcionar no pressuposto de que você recebeu permissão de leitura/gravação. 
    
 _lpulObjType_
  
> [out] Um ponteiro para o tipo de objeto aberto.
    
 _lppUnk_
  
> [out] Um ponteiro para o ponteiro para o objeto aberto.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Coment�rios

MAPI chama o método **IMSLogon::OpenEntry** para abrir uma pasta ou uma mensagem em um armazenamento de mensagens. MAPI passa o identificador de entrada do objeto a ser aberto. O provedor de armazenamento de mensagem deve retornar um ponteiro que permite o acesso ao objeto especificado no parâmetro _lppUnk_ . 
  
Antes de chamadas de MAPI **IMSLogon::OpenEntry**, primeiro determina que o identificador de entrada da pasta ou determinada mensagem corresponde a um registrado por esse provedor de repositório de mensagem. Para obter mais informações sobre como registrar os provedores de armazenamento de identificadores de entrada, consulte [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).
  
 **IMSLogon::OpenEntry** é idêntico ao método [IMsgStore::OpenEntry](imsgstore-openentry.md) do objeto de repositório de mensagem, exceto que o cliente não chamar **IMSLogon::OpenEntry**; As chamadas de MAPI **IMSLogon::OpenEntry** quando ele processa um método **IMAPISession::OpenEntry** . Objetos abertos usando **IMSLogon::OpenEntry** devem ser tratados exatamente como objetos abertos usando a mensagem armazenam objeto; em particular, objetos abertos usando essa chamada devem ser invalidados quando o objeto de repositório da mensagem for lançado. 
  
## <a name="see-also"></a>Confira também



[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMSLogon: IUnknown](imslogoniunknown.md)

