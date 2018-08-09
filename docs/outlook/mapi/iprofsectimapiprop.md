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
ms.openlocfilehash: c0653caec5f3cac531206e1bb9c4330cac5f3133
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767650"
---
# <a name="iprofsect--imapiprop"></a>IProfSect : IMAPIProp

  
  
**Aplica-se a**: Outlook 
  
Funciona com as propriedades dos objetos de seção de perfil. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapix.h  <br/> |
|Expostos pelo:  <br/> |Objetos de seção de perfil  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
|Identificador de interface:  <br/> |IID_IProfSect  <br/> |
|Tipo de ponteiro:  <br/> |LPPROFSECT  <br/> |
|Modelo de transação:  <br/> |Nontransacted  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

Essa interface não tem quaisquer métodos exclusivos.
  
|**Propriedades necessárias**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))  <br/> |Somente leitura  <br/> |
   
## <a name="notes-to-callers"></a>Notas para chamadores

A interface **IProfSect** não tem quaisquer métodos exclusivos de seu próprio, mas você pode chamar o perfil de métodos de [IMAPIProp](imapipropiunknown.md) da seção. Há algumas diferenças entre a implementação de **IProfSect** e outras implementações de **IMAPIProp**:
  
- **IProfSect** não oferece suporte a um modelo de transação. 
    
- **IProfSect** não oferece suporte a propriedades nomeadas. 
    
- **IProfSect** reserva-se o intervalo de identificador 0x67F0 para 0x67ff para propriedades seguras. 
    
Suporte a um modelo de transação não significa que todas as alterações feitas a seguir de uma seção de perfil chamadas para o [IMAPIProp::CopyProps](imapiprop-copyprops.md) e [IMAPIProp::CopyTo](imapiprop-copyto.md) métodos ocorrerem imediatamente. Chamadas para o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) êxito, mas não realmente salvar quaisquer alterações. 
  
Para se proteger contra alterações que ocorrem prematuramente, provedores de serviços precisam fazer cópias das suas seções de perfil que são exibidas para usuários por meio de folhas de propriedades. Folhas de propriedades devem trabalhar com a cópia, em vez de seção perfil real. Quando o usuário clica no botão **Okey** para verificar se as alterações são precisas, as alterações podem ser salvas para a seção perfil real. 
  
Para implementar uma folha de propriedades por meio de uma seção de perfil copiado, use o procedimento a seguir:
  
1. Abra a seção de perfil chamando o método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) ou [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) . 
    
2. Chamar a função [CreateIProp](createiprop.md) para recuperar um objeto de dados de propriedade — um objeto que dá suporte à interface **IPropData** . 
    
3. Chame o método de [IMAPIProp::CopyTo](imapiprop-copyto.md) da seção perfil para copiar as propriedades que serão exibidas na folha de propriedades da seção de perfil para o objeto de dados de propriedade. 
    
4. Chame o método [IMAPISupport::DoConfigPropSheet](imapisupport-doconfigpropsheet.md) para solicitar que o provedor de serviço exibir uma folha de propriedades e passar um ponteiro para o objeto de dados de propriedade no parâmetro _lpConfigData_ . 
    
5. Quando o usuário salva alterações às propriedades de configuração na folha de propriedades, chame o método [IMAPIProp::CopyTo](imapiprop-copyto.md) para copiar as propriedades do objeto de dados de propriedade voltar para a seção de perfil. 
    
As seções de perfil, ao contrário de outros objetos, não têm suporte a propriedades nomeadas. Os métodos [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) e [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) retornam MAPI_E_NO_SUPPORT se forem chamados em um objeto de seção de perfil. Se você usar o método [IMAPIProp::SetProps](imapiprop-setprops.md) para definir os identificadores de propriedade do intervalo acima 0x8000, o tipo de propriedade PT_ERROR será retornado. 
  
As seções de perfil reservam o intervalo de identificador 0x67F0 para 0x67FF para propriedades seguras. Provedores de serviços podem usar este intervalo para armazenar senhas e outras credenciais específicas do provedor. Propriedades nesse intervalo não são retornadas na lista completa de propriedades quando NULL é passada no parâmetro _lpPropTag_ do método [IMAPIProp::GetProps](imapiprop-getprops.md) , nem são retornados no parâmetro _lppPropTagArray_ do [ IMAPIProp::GetPropList](imapiprop-getproplist.md) método. Propriedades protegidas devem ser solicitadas especificamente por seus identificadores. 
  
MAPI fornece uma seção de perfil com MUID_PROFILE_INSTANCE constante codificadas como seu identificador e **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) como sua propriedade única. MAPI garante que o valor da propriedade **PR_SEARCH_KEY** sejam exclusivo entre todos os perfis criados. Use **PR_SEARCH_KEY** em vez de **PR_PROFILE_NAME** quando exclusividade é importante, porque é possível perfil excluída a ser seguidos por outro perfil com o mesmo nome. 
  
Para obter mais informações sobre como usar as seções de perfil, consulte [Administrando perfis e serviços de mensagem](administering-profiles-and-message-services.md).
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

