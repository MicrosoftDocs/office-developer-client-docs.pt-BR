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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416297"
---
# <a name="imslogonopenentry"></a>IMSLogon::OpenEntry

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre uma pasta ou objeto message e retorna um ponteiro para o objeto para fornecer mais acesso. 
  
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
  
> [in] O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Um ponteiro para o endereço do identificador de entrada do objeto de pasta ou mensagem a ser aberto. 
    
 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) do objeto. Passar NULL indica que o objeto é lançado para a interface padrão para esse objeto. O  _parâmetro lpInterface_ também pode ser definido como um identificador para uma interface apropriada para o objeto. 
    
 _ulOpenFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como o objeto é aberto. Os sinalizadores a seguir podem ser definidos:
    
MAPI_BEST_ACCESS 
  
> O objeto deve ser aberto com as permissões máximas permitidas para o usuário e o máximo de permissões do aplicativo cliente. Por exemplo, se o cliente tiver permissão de leitura/gravação, o objeto será aberto com permissão de leitura/gravação; se o cliente tiver permissão somente leitura, o objeto será aberto com permissão somente leitura. O cliente pode recuperar o nível de permissão, PR_ACCESS_LEVEL **propriedade** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
    
MAPI_DEFERRED_ERRORS 
  
> A chamada tem permissão para ser bem-sucedida, mesmo se o objeto subjacente não estiver disponível para o aplicativo de chamada. Se o objeto não estiver disponível, uma chamada subsequente para o objeto poderá retornar um erro.
    
MAPI_MODIFY 
  
> Solicita permissão de leitura/gravação. Por padrão, os objetos são criados com permissão somente leitura e os clientes não devem trabalhar com a suposição de que a permissão de leitura/gravação foi concedida. 
    
 _lpulObjType_
  
> [out] Um ponteiro para o tipo do objeto aberto.
    
 _lppUnk_
  
> [out] Um ponteiro para o ponteiro para o objeto aberto.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

O MAPI chama **o método IMSLogon::OpenEntry** para abrir uma pasta ou uma mensagem em um armazenamento de mensagens. O MAPI passa o identificador de entrada do objeto a ser aberto. O provedor de armazenamento de mensagens deve retornar um ponteiro que permita mais acesso ao objeto especificado no _parâmetro lppUnk._ 
  
Antes de o MAPI chamar **IMSLogon::OpenEntry**, ele primeiro determina que o identificador de entrada de pasta ou mensagem determinado corresponde a um registrado por esse provedor de armazenamento de mensagens. Para obter mais informações sobre como os provedores de armazenamento registram identificadores de entrada, consulte [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).
  
 **IMSLogon::OpenEntry** é idêntico ao método [IMsgStore::OpenEntry](imsgstore-openentry.md) do objeto de repositório de mensagens, exceto que o cliente não chama **IMSLogon::OpenEntry**; MAPI calls **IMSLogon::OpenEntry** when it processes an **IMAPISession::OpenEntry** method. Os objetos abertos usando **IMSLogon::OpenEntry** devem ser tratados exatamente como objetos abertos usando o objeto de armazenamento de mensagens; em particular, os objetos abertos usando essa chamada devem ser invalidados quando o objeto do armazenamento de mensagens é liberado. 
  
## <a name="see-also"></a>Confira também



[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

