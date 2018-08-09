---
title: IMAPISupportOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenTemplateID
api_type:
- COM
ms.assetid: 532f7af0-b2cc-49dd-b1de-e3ec1dc9a3e7
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f99843bcdf3689acad72145a33d6a9804175a413
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767277"
---
# <a name="imapisupportopentemplateid"></a>IMAPISupport::OpenTemplateID

  
  
**Aplica-se a**: Outlook 
  
Abre uma entrada de destinatários em um provedor de catálogo de endereço estrangeiro.
  
```cpp
HRESULT OpenTemplateID(
ULONG cbTemplateID,
LPENTRYID lpTemplateID,
ULONG ulTemplateFlags,
LPMAPIPROP lpMAPIPropData,
LPCIID lpInterface,
LPMAPIPROP FAR * lppMAPIPropNew,
LPMAPIPROP lpMAPIPropSibling
);
```

## <a name="parameters"></a>Parâmetros

 _cbTemplateID_
  
> [in] A contagem de bytes do identificador de modelo apontado pela _lpTemplateID_. 
    
 _lpTemplateID_
  
> [in] Um ponteiro para o identificador de modelo de propriedade **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) da entrada do destinatário a serem abertas.
    
 _ulTemplateFlags_
  
> [in] Uma bitmask dos sinalizadores usados para descrever como abrir a entrada. O seguinte sinalizador pode ser definido:
    
FILL_ENTRY 
  
> Uma nova entrada está sendo criada. Quando o provedor estrangeiro recebe a chamada de [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md) subsequente de MAPI, pode controlar como a entrada é criada, modificando propriedades apontadas pelo parâmetro _lpMAPIPropData_ ou, retornando uma interface específica implementação em _lppMAPIPropNew_ para controlar como propriedades para a nova entrada estiverem definidas. 
    
 _lpMAPIPropData_
  
> [in] Um ponteiro para a implementação de interface que o chamador usa para acessar a entrada. Esta é a implementação que o provedor estrangeiro pode quebrar automaticamente com sua própria implementação e retornar no parâmetro _lppMAPIPropNew_ . O parâmetro _lpMAPIPropData_ deve apontar para uma implementação de interface de leitura/gravação que derive da [IMAPIProp: IUnknown](imapipropiunknown.md) e dá suporte à interface sendo solicitada no parâmetro _lpInterface_ . 
    
 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface que será usada para acessar a entrada. O parâmetro _lppMAPIPropNew_ aponta para uma interface do tipo especificado pelo _lpInterface_. Passar NULL retorna a interface padrão para um usuário de mensagens, IID_IMailUser. 
    
 _lppMAPIPropNew_
  
> [out] Um ponteiro para a implementação de interface que o provedor estrangeiro fornece para acessar a entrada.
    
 _lpMAPIPropSibling_
  
> Reservado; deve ser NULL.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O processo de ligação foi bem-sucedida.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> O provedor de catálogo de endereço estrangeiro não existe.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::OpenTemplateID** é implementado apenas para objetos de suporte do provedor de catálogo de endereços. **OpenTemplateID** é chamado somente por provedores de catálogo de endereços que podem atuar como hosts para entradas que pertencem a outros provedores de catálogo de endereços, também conhecido como estrangeira provedores. Provedores de host chamarem **OpenTemplateID** para abrir uma entrada externa, o que ocorre quando os dados no provedor de host são vinculados ao código no provedor estrangeiro. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Chame **OpenTemplateID** somente se você oferecer suporte ao armazenamento de entradas com identificadores de modelo de provedores de catálogo de endereço estrangeiro. Tal suporte coloca as implementações [IABContainer::CreateEntry](iabcontainer-createentry.md) e [IABLogon::OpenEntry](iablogon-openentry.md) requisitos adicionais. Para obter mais informações, consulte as descrições desses métodos e [atuando como um provedor de catálogo de endereço de Host](acting-as-a-host-address-book-provider.md).
  
Se a chamada **OpenTemplateID** retornar como a interface acoplada a mesma implementação de objeto de propriedade que você passado, você pode liberar sua referência para seu objeto de propriedade. Isso ocorre porque o provedor estrangeiro chamou o método do objeto **AddRef** para manter sua própria referência. Se o provedor estrangeiro não precisa manter uma referência ao objeto de propriedade, **OpenTemplateID** retornará o objeto não acoplado property. 
  
Se **OpenTemplateID** falhar com MAPI_E_UNKNOWN_ENTRYID, tente continuar tratando-se a entrada como somente leitura. 
  
## <a name="see-also"></a>Confira também



[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[Propriedade canônica PidTagTemplateid](pidtagtemplateid-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

