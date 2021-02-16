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
  
> [in] A contagem dos bytes no identificador de entrada apontado pelo parâmetro _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada de um modelo para criar novas entradas de um tipo específico. 
    
 _ulCreateFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como a criação de entrada é realizada. Os sinalizadores a seguir podem ser definidos:
    
CREATE_CHECK_DUP_LOOSE 
  
> Um nível solto de verificação de entrada duplicada deve ser executado. A implementação da verificação de entrada com duplicação livre é específica do provedor. Por exemplo, um provedor pode definir uma combinação livre como qualquer uma das duas entradas que tenham o mesmo nome de exibição.
    
CREATE_CHECK_DUP_STRICT 
  
> Um nível estrito de verificação de entrada duplicada deve ser executado. A implementação da verificação de entrada duplicada estrita é específica do provedor. Por exemplo, um provedor pode definir uma combinação estrita como qualquer uma das duas entradas que tenham o mesmo nome de exibição e endereço de mensagens.
    
CREATE_REPLACE 
  
> Uma nova entrada deve substituir uma existente se for determinado que as duas são duplicatas.
    
 _lppMAPIPropEntry_
  
> [out] Um ponteiro para um ponteiro para a entrada recém-criada.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A nova entrada foi criada com êxito.
    
## <a name="remarks"></a>Comentários

O **método IABContainer::CreateEntry** cria uma nova entrada de um tipo específico no contêiner especificado, retornando um ponteiro para uma implementação de interface para mais acesso à entrada. A nova entrada é criada usando um modelo que foi selecionado na lista de modelos disponíveis do contêiner publicada em sua tabela única. Os chamadores acessam a tabela única de um contêiner chamando seu método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) e solicitando a propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Todos os contêineres que suportam **o método IABContainer::CreateEntry** devem ser modificáveis. Defina o sinalizador de AB_MODIFIABLE contêiner em sua **propriedade PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) para indicar que ele é modificável. 
  
Você deve dar suporte a todos os _sinalizadores ulCreateFlags._ No entanto, a interpretação e o uso desses sinalizadores são específicos de implementação— ou seja, você pode determinar o que a semântica de CREATE_CHECK_DUP_LOOSE e CREATE_CHECK_DUP_STRICT significa no contexto de sua implementação. Se você não puder ou não determinar se uma entrada é uma duplicata, sempre permita que a entrada seja criada. 
  
Alguns provedores implementam verificação estrita de entrada, correspondendo ao nome para exibição, endereço de mensagens e chave de pesquisa em uma entrada; outros provedores limitam a corresponder ao nome de exibição e ao endereço. A verificação de entrada solta geralmente é implementada verificando apenas o nome de exibição. 
  
## <a name="notes-to-host-address-book-provider-implementers"></a>Observações para implementadores do provedor de agendamento de endereço de host

Se o contêiner puder criar entradas a partir dos modelos de outros provedores, sua implementação de **CreateEntry** deverá fornecer armazenamento para algumas ou todas as propriedades associadas às entradas criadas. Por exemplo, se você fornecer armazenamento para a propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) de uma entrada, poderá gerar sua caixa de diálogo de detalhes sem precisar depender do provedor estrangeiro. 
  
Se o contêiner puder criar entradas que deem suporte **à PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)), sua implementação de **CreateEntry** deverá fazer o seguinte: 
  
1. Chame o [método IMAPISupport::OpenTemplateID.](imapisupport-opentemplateid.md) **OpenTemplateID** permite que o código do provedor externo para a entrada se a bind à nova entrada que está sendo criada. Provedores externos suportam esse processo de associação para manter o controle sobre entradas criadas a partir de seus modelos para os contêineres de provedores de agendamento de endereço host. 
    
2. Execute qualquer inicialização necessária e preencha o novo objeto com todas as propriedades da entrada no provedor estrangeiro que o objeto retornou no parâmetro  _lppMAPIPropNew_ de **OpenTemplateID**.
    
Se **OpenTemplateID** for bem-sucedido, copie as propriedades para a implementação apontada pelo parâmetro _lppMAPIPropNew_ em vez de diretamente para a implementação apontada pelo parâmetro _lpMAPIPropData._ Inicialize a nova entrada para uso offline como faria com qualquer outra entrada de um provedor estrangeiro. 
  
Se **OpenTemplateID** retornar um erro, **CreateEntry** deve falhar. Não permitir que a entrada seja criada. Como o provedor externo pode fazer suposições sobre os dados em seu provedor, não crie uma entrada com um identificador de modelo que não tenha sido vinculado com êxito ao provedor estrangeiro. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando **CreateEntry** retorna, você pode ou não ser capaz de acessar imediatamente o identificador de entrada para a nova entrada. Alguns provedores de agendas não o disponibilizam até que você tenha chamado o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da nova entrada. 
  
Embora sinalizadores de verificação duplicados sejam passados como parâmetros para **CreateEntry**, a operação de verificação duplicada não ocorrerá **até que SaveChanges** seja chamado. Portanto, erros relacionados, como MAPI_E_COLLISION, que indica que foi feita uma tentativa de criar uma entrada já existente, são retornados por **SaveChanges** em vez de **CreateEntry**.
  
## <a name="see-also"></a>Confira também



[IABContainer::CopyEntries](iabcontainer-copyentries.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[Propriedade canônica PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

