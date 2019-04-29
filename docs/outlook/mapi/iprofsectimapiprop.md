---
title: IProfSect IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfSect
api_type:
- COM
ms.assetid: 4e704044-5230-4521-a0d2-b7c2f981c954
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 99ce944bec94a1e832f77fa8b0916ac1c76f6dc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406595"
---
# <a name="iprofsect--imapiprop"></a>IProfSect : IMAPIProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Funciona com as propriedades dos objetos seção de perfil. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapix. h  <br/> |
|Exposto por:  <br/> |Objetos de seção de perfil  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
|Identificador de interface:  <br/> |IID_IProfSect  <br/> |
|Tipo de ponteiro:  <br/> |LPPROFSECT  <br/> |
|Modelo de transação:  <br/> |Não-Transacted  <br/> |
   
## <a name="vtable-order"></a>Vtable order

Esta interface não tem nenhum método exclusivo.
  
|**Propriedades necessárias**|**Acesso**|
|:-----|:-----|
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))  <br/> |Somente leitura  <br/> |
   
## <a name="notes-to-callers"></a>Notas para chamadores

A interface **IProfSect** não tem nenhum método exclusivo, mas você pode chamar os métodos [IMAPIProp](imapipropiunknown.md) da seção de perfil. Há algumas diferenças entre a implementação do **IProfSect** e outras implementações do **IMAPIProp**:
  
- **IProfSect** não dá suporte a um modelo de transação. 
    
- **IProfSect** não dá suporte a propriedades nomeadas. 
    
- **IProfSect** reserva o intervalo de identificadores 0x67F0 para o 0x67ff para propriedades seguras. 
    
Não oferecer suporte a um modelo de transação significa que todas as alterações feitas em uma seção de perfil seguindo as chamadas para os métodos [IMAPIProp:: CopyProps](imapiprop-copyprops.md) e [IMAPIProp:: CopyTo](imapiprop-copyto.md) ocorrem imediatamente. As chamadas para o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) são bem-sucedidas, mas não realmente salvam as alterações. 
  
Para ser protegido contra alterações que ocorrem prematuramente, os provedores de serviços precisam fazer cópias de suas seções de perfil que são exibidas aos usuários por meio de folhas de propriedades. As folhas de propriedades devem funcionar com a cópia, em vez da seção real de perfil. Quando o usuário clica no botão **OK** para verificar se as alterações são precisas, as alterações podem ser salvas na seção perfil real. 
  
Para implementar uma folha de propriedades usando uma seção de perfil copiada, use o procedimento a seguir:
  
1. Abra a seção perfil chamando o método [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) ou [IProviderAdmin:: OpenProfileSection](iprovideradmin-openprofilesection.md) . 
    
2. Chame a função [CreateIProp](createiprop.md) para recuperar um objeto de dados de propriedade — um objeto que oferece suporte à interface **IPropData** . 
    
3. Chame o método [IMAPIProp:: CopyTo](imapiprop-copyto.md) da seção de perfil para copiar as propriedades que serão exibidas na folha de propriedades da seção perfil para o objeto de dados de propriedade. 
    
4. Chame o método [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) para solicitar que o provedor de serviços exiba uma folha de propriedades e passe um ponteiro para o objeto de dados de propriedade no parâmetro _lpConfigData_ . 
    
5. Quando o usuário salva as alterações nas propriedades de configuração na folha de propriedades, chame o método [IMAPIProp:: CopyTo](imapiprop-copyto.md) para copiar as propriedades do objeto de dados de propriedade de volta para a seção perfil. 
    
Seções de perfil, ao contrário de outros objetos, não dão suporte a propriedades nomeadas. Os métodos [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) e [IMAPIProp:: GETNAMESFROMIDS](imapiprop-getnamesfromids.md) retornam MAPI_E_NO_SUPPORT se forem chamados em um objeto section de perfil. Se você usar o método [IMAPIProp::](imapiprop-setprops.md) SetProps para definir identificadores de propriedade no intervalo acima de 0x8000, o tipo de propriedade PT_ERROR será retornado. 
  
Seções de perfil Reserve o intervalo de identificadores 0x67F0 para 0x67FF para propriedades seguras. Os provedores de serviços podem usar esse intervalo para armazenar senhas e outras credenciais específicas do provedor. As propriedades neste intervalo não são retornadas na lista completa de propriedades quando NULL é passado no parâmetro _lpPropTag_ do método [IMAPIProp::](imapiprop-getprops.md) GetProps, nem são retornados no parâmetro _lppPropTagArray_ do [ Método IMAPIProp::](imapiprop-getproplist.md) Getproplist. As propriedades seguras devem ser solicitadas especificamente por seus identificadores. 
  
O MAPI fornece uma seção de perfil com a constante codificada MUID_PROFILE_INSTANCE como seu identificador e **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) como sua única propriedade. O MAPI garante que o valor da propriedade **PR_SEARCH_KEY** será exclusivo entre todos os perfis criados. Use **PR_SEARCH_KEY** em vez de **PR_PROFILE_NAME** quando a exclusividade for importante, pois é possível que um perfil excluído seja seguido por outro perfil com o mesmo nome. 
  
Para obter mais informações sobre como usar seções de perfil, consulte [Administração de perfis e serviços de mensagens](administering-profiles-and-message-services.md).
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

