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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 544aaaace18a9d26972e6484803b63a1ee7060fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317280"
---
# <a name="imslogonopenentry"></a>IMSLogon::OpenEntry

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre uma pasta ou um objeto Message e retorna um ponteiro para o objeto para fornecer mais acesso. 
  
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

## <a name="parameters"></a>Parâmetros

 _cbEntryID_
  
> no O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> no Um ponteiro para o endereço do identificador de entrada do objeto Folder ou Message a ser aberto. 
    
 _lpInterface_
  
> no Um ponteiro para o identificador de interface (IID) do objeto. Passar NULL indica que o objeto é convertido na interface padrão para tal objeto. O parâmetro _lpInterface_ também pode ser definido como um identificador para uma interface apropriada para o objeto. 
    
 _ulOpenFlags_
  
> no Uma bitmask de sinalizadores que controla como o objeto é aberto. Os seguintes sinalizadores podem ser definidos:
    
MAPI_BEST_ACCESS 
  
> O objeto deve ser aberto com as permissões máximas permitidas para o usuário e as permissões máximas do aplicativo cliente. Por exemplo, se o cliente tem permissão de leitura/gravação, o objeto é aberto com permissão de leitura/gravação; Se o cliente tem permissão somente leitura, o objeto é aberto com permissão somente leitura. O cliente pode recuperar o nível de permissão obtendo a propriedade **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
    
MAPI_DEFERRED_ERRORS 
  
> A chamada terá permissão para ter êxito, mesmo se o objeto subjacente não estiver disponível para o aplicativo de chamada. Se o objeto não estiver disponível, uma chamada subsequente para o objeto poderá retornar um erro.
    
MAPI_MODIFY 
  
> Solicita permissão de leitura/gravação. Por padrão, os objetos são criados com permissão somente leitura e os clientes não devem funcionar na pressuposição de que a permissão de leitura/gravação tenha sido concedida. 
    
 _lpulObjType_
  
> bota Um ponteiro para o tipo do objeto aberto.
    
 _lppUnk_
  
> bota Um ponteiro para o ponteiro para o objeto aberto.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

MAPI chama o método **IMSLogon:: OpenEntry** para abrir uma pasta ou uma mensagem em um repositório de mensagens. MAPI passa no identificador de entrada do objeto a ser aberto. O provedor de repositório de mensagens deve retornar um ponteiro que permita o acesso adicional ao objeto especificado no parâmetro _lppUnk_ . 
  
Antes de chamadas MAPI **IMSLogon:: OpenEntry**, ele primeiro determina que o identificador de entrada de pasta ou mensagem fornecido corresponde a um registrado por este provedor de repositório de mensagens. Para obter mais informações sobre como os provedores de repositório registram identificadores de entrada, consulte [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md).
  
 **IMSLogon:: OpenEntry** é idêntico ao método [IMsgStore:: OpenEntry](imsgstore-openentry.md) do objeto do repositório de mensagens, exceto pelo fato de que o cliente não chama **IMSLogon:: OpenEntry**; Chamadas MAPI **IMSLogon:: OpenEntry** quando processa um método **IMAPISession:: OpenEntry** . Os objetos abertos com o uso de **IMSLogon:: OpenEntry** devem ser tratados exatamente da mesma forma que os objetos abertos usando o objeto de repositório de mensagens; em particular, os objetos abertos usando essa chamada devem ser invalidados quando o objeto do repositório de mensagens é liberado. 
  
## <a name="see-also"></a>Confira também



[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

