---
title: IABContainerCreateEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.CreateEntry
api_type:
- COM
ms.assetid: ea1daf74-d9e3-4304-bf5d-889afeea6ae9
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9f80130279e3437dd9be947de97d3f0d4181165e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411271"
---
# <a name="iabcontainercreateentry"></a>IABContainer::CreateEntry

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria uma nova entrada, que pode ser um usuário de mensagens, uma lista de distribuição ou outro contêiner.
  
```cpp
HRESULT CreateEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulCreateFlags,
  LPMAPIPROP FAR * lppMAPIPropEntry
);
```

## <a name="parameters"></a>Parâmetros

 _cbEntryID_
  
> no A contagem dos bytes no identificador de entrada apontados pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> no Um ponteiro para o identificador de entrada de um modelo para a criação de novas entradas de um determinado tipo. 
    
 _ulCreateFlags_
  
> no Uma bitmask de sinalizadores que controla como a criação de entrada é realizada. Os seguintes sinalizadores podem ser definidos:
    
CREATE_CHECK_DUP_LOOSE 
  
> Um nível flexível de verificação de entrada duplicada deve ser executado. A implementação da verificação de entrada duplicada resolta é específica do provedor. Por exemplo, um provedor pode definir uma correspondência frouxa como qualquer duas entradas com o mesmo nome de exibição.
    
CREATE_CHECK_DUP_STRICT 
  
> Um nível estrito de verificação de entrada duplicada deve ser executado. A implementação de verificação de entrada duplicada estrita é específica do provedor. Por exemplo, um provedor pode definir uma correspondência estrita como qualquer duas entradas que tenham o mesmo nome de exibição e endereço de mensagens.
    
CREATE_REPLACE 
  
> Uma nova entrada deve substituir uma existente se for determinado que as duas são duplicatas.
    
 _lppMAPIPropEntry_
  
> bota Um ponteiro para um ponteiro para a entrada recém-criada.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A nova entrada foi criada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IABContainer:: createentry** cria uma nova entrada de um tipo específico no contêiner especificado, retornando um ponteiro para uma implementação de interface para acesso adicional à entrada. A nova entrada é criada usando um modelo que foi selecionado na lista de modelos disponíveis do contêiner publicada em sua tabela única. Os chamadores acessam a tabela única de um contêiner chamando o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) e solicitando a propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Todos os contêineres compatíveis com o método **IABContainer:: createentry** devem ser modificáveis. Defina o sinalizador AB_MODIFIABLE de seu contêiner em sua propriedade **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) para indicar que ele é modificável. 
  
Você deve dar suporte a todos os sinalizadores _ulCreateFlags_ . No enTanto, a interpretação e o uso desses sinalizadores são específicos de implementação, ou seja, você pode determinar quais são as semânticas de CREATE_CHECK_DUP_LOOSE e CREATE_CHECK_DUP_STRICT no contexto da sua implementação. Se você não puder ou não determinar se uma entrada é uma duplicata, sempre permita que a entrada seja criada. 
  
Alguns provedores implementam a verificação de entrada estrita, combinando o nome para exibição, o endereço de mensagens e a chave de pesquisa em uma entrada; outros provedores limitam a correspondência para exibir o nome e o endereço. A verificação de entrada flexível geralmente é implementada verificando apenas o nome de exibição. 
  
## <a name="notes-to-host-address-book-provider-implementers"></a>Observações para implementadores do provedor de catálogo de endereços do host

Se o seu contêiner pode criar entradas dos modelos de outros provedores, sua implementação de **createentry** deve fornecer armazenamento para algumas ou todas as propriedades associadas às entradas criadas. Por exemplo, se você fornecer armazenamento para a propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) de uma entrada, poderá gerar sua caixa de diálogo detalhes sem precisar depender do provedor estrangeiro. 
  
Se o seu contêiner pode criar entradas que suportam a propriedade **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)), sua implementação de createentry deve fazer o seguinte: **** 
  
1. Chame o método [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md) . **OpenTemplateID** habilita o código do provedor estrangeiro para a entrada vincular à nova entrada que está sendo criada. Os provedores estrangeiros dão suporte a esse processo de associação para manter o controle sobre as entradas criadas de seus modelos nos contêineres de provedores de catálogo de endereços de host. 
    
2. Execute qualquer inicialização necessária e preencha o novo objeto com todas as propriedades da entrada no provedor estrangeiro que o objeto retornou no parâmetro _lppMAPIPropNew_ de **OpenTemplateID**.
    
Se o **OpenTemplateID** tiver êxito, copie as propriedades para a implementação indicada pelo parâmetro _lppMAPIPropNew_ , em vez de diretamente na implementação indicada pelo parâmetro _lpMAPIPropData_ . Inicialize a nova entrada para uso offline como faria com qualquer outra entrada de um provedor estrangeiro. 
  
Se **OpenTemplateID** retornar um erro, **createentry** deverá falhar. Não permite que a entrada seja criada. Como o provedor estrangeiro pode fazer suposições sobre os dados no seu provedor, não crie uma entrada com um identificador de modelo que não tenha sido vinculado com êxito ao provedor estrangeiro. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando **createentry** retornar, você poderá ou não conseguir acessar imediatamente o identificador de entrada para a nova entrada. Alguns provedores do catálogo de endereços não o disponibilizam até depois de chamar o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) da nova entrada. 
  
Embora os sinalizadores de verificação duplicados sejam passados **** como parâmetros para createentry, a operação de verificação de duplicatas não ocorre até que **SaveChanges** seja chamado. Portanto, erros relacionados como MAPI_E_COLLISION, que indicam que uma tentativa foi feita para criar uma entrada já existente, são retornados por **SaveChanges** , e não **** por createentry.
  
## <a name="see-also"></a>Confira também



[IABContainer::CopyEntries](iabcontainer-copyentries.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[Propriedade canônica PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

