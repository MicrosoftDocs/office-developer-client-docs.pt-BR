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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 07aa508b473f4a87d5b4909f83771549c301a600
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326359"
---
# <a name="imapisupportopentemplateid"></a>IMAPISupport::OpenTemplateID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre uma entrada de destinatário em um provedor de catálogo de endereços externo.
  
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
  
> no A contagem de bytes no identificador de modelo apontado por _lpTemplateID_. 
    
 _lpTemplateID_
  
> no Um ponteiro para a propriedade de identificador de **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) da entrada de destinatário a ser aberta.
    
 _ulTemplateFlags_
  
> no Uma bitmask de sinalizadores usados para descrever como abrir a entrada. O seguinte sinalizador pode ser definido:
    
FILL_ENTRY 
  
> Uma nova entrada está sendo criada. Quando o provedor estrangeiro recebe a chamada [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md) subsequente de MAPI, ele pode controlar como a entrada é criada modificando as propriedades apontadas pelo parâmetro _lpMAPIPropData_ ou retornando uma interface específica implementação no _lppMAPIPropNew_ para controlar como as propriedades da nova entrada são definidas. 
    
 _lpMAPIPropData_
  
> no Um ponteiro para a implementação de interface que o chamador usa para acessar a entrada. Esta é a implementação que o provedor externo pode quebrar com sua própria implementação e retornar no parâmetro _lppMAPIPropNew_ . O parâmetro _lpMAPIPropData_ deve apontar para uma implementação de interface de leitura/gravação que deriva de [IMAPIProp: IUnknown](imapipropiunknown.md) e dá suporte à interface que está sendo solicitada no parâmetro _lpInterface_ . 
    
 _lpInterface_
  
> no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar a entrada. O parâmetro _lppMAPIPropNew_ aponta para uma interface do tipo especificado por _lpInterface_. Passar nulo retorna a interface padrão de um usuário de mensagens, IID_IMailUser. 
    
 _lppMAPIPropNew_
  
> bota Um ponteiro para a implementação de interface que o provedor externo fornece para acessar a entrada.
    
 _lpMAPIPropSibling_
  
> Serve deve ser nulo.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O processo de associação foi bem-sucedido.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> O provedor do catálogo de endereços externo não existe.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport:: OpenTemplateID** é implementado apenas para objetos de suporte do provedor de catálogo de endereços. **OpenTemplateID** é chamado apenas por provedores de catálogo de endereços que podem atuar como hosts para entradas que pertencem a outros provedores de catálogo de endereços, também conhecidos como provedores estrangeiros. Os provedores de host chamam **OpenTemplateID** para abrir uma entrada externa, que ocorre quando os dados no provedor de host estão vinculados ao código no provedor estrangeiro. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Chame **OpenTemplateID** somente se você oferecer suporte ao armazenamento de entradas com identificadores de modelo de provedores de catálogos de endereços externos. Esse suporte impõe requisitos adicionais em suas implementações [IABContainer:: createentry](iabcontainer-createentry.md) e [IABLogon:: OpenEntry](iablogon-openentry.md) . Para obter mais informações, consulte as descrições desses métodos e [atuando como um provedor de catálogo de endereços de host](acting-as-a-host-address-book-provider.md).
  
Se a chamada **OpenTemplateID** retornar como interface associada à mesma implementação do objeto Property que você aprovou, você pode liberar sua referência para o objeto Property. Isso ocorre porque o provedor estrangeiro chamou o método **AddRef** do objeto para manter sua própria referência. Se o provedor estrangeiro não precisar manter uma referência ao objeto Property, **OpenTemplateID** retornará o objeto Property não associado. 
  
Se o **OpenTemplateID** falhar com o MAPI_E_UNKNOWN_ENTRYID, tente continuar tratando a entrada como somente leitura. 
  
## <a name="see-also"></a>Confira também



[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[Propriedade canônica PidTagTemplateid](pidtagtemplateid-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

