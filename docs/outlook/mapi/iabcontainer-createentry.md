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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: acf9cee9bf0713b909b0d82fc606b015ac28474e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766846"
---
# <a name="iabcontainercreateentry"></a>IABContainer::CreateEntry

  
  
**Aplica-se a**: Outlook 
  
Cria uma nova entrada, que pode ser um usuário de mensagens, uma lista de distribuição ou outro contêiner.
  
```cpp
HRESULT CreateEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulCreateFlags,
  LPMAPIPROP FAR * lppMAPIPropEntry
);
```

## <a name="parameters"></a>Par�metros

 _cbEntryID_
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada de um modelo para a criação de novas entradas de um determinado tipo. 
    
 _ulCreateFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como a criação de entrada é executada. Sinalizadores a seguir podem ser definidos:
    
CREATE_CHECK_DUP_LOOSE 
  
> Um nível afastado de verificação de entrada duplicada deve ser realizado. A implementação de verificação de entrada duplicada afastada é específico do provedor. Por exemplo, um provedor pode definir uma correspondência afastada conforme qualquer duas entradas que têm o mesmo nome de exibição.
    
CREATE_CHECK_DUP_STRICT 
  
> Um nível estrito de verificação de entrada duplicada deve ser realizado. A implementação de verificação de entrada duplicada strict é específico do provedor. Por exemplo, um provedor pode definir uma correspondência estrita como qualquer duas entradas que têm ambas o mesmo nome e endereço de mensagens são exibidos.
    
CREATE_REPLACE 
  
> Uma nova entrada deve substituir um já existente, se for determinado que as duas versões sejam duplicatas.
    
 _lppMAPIPropEntry_
  
> [out] Um ponteiro para um ponteiro para a entrada recém-criado.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A nova entrada foi criada com êxito.
    
## <a name="remarks"></a>Coment�rios

O método **IABContainer::CreateEntry** cria uma nova entrada de um determinado tipo no contêiner especificado, retornando um ponteiro para uma implementação de interface para acesso à entrada. A nova entrada é criada usando um modelo que foi selecionado na lista do contêiner dos modelos disponíveis publicado em sua tabela único. Os chamadores acessar a tabela de únicos de um contêiner chamando seu método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) e solicitar a propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Todos os contêineres que suportam o método **IABContainer::CreateEntry** devem ser pode ser modificados. Defina sinalizador AB_MODIFIABLE do seu contêiner na sua propriedade **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) para indicar que ela é modificável. 
  
Você deve oferecer suporte a todos os sinalizadores _ulCreateFlags_ . No entanto, a interpretação e usar esses sinalizadores é específico da implementação — ou seja, você pode determinar o significado a semântica de CREATE_CHECK_DUP_LOOSE e CREATE_CHECK_DUP_STRICT no contexto da sua implementação. Se você não pode ou não determinam se uma entrada é uma duplicata, sempre permita a entrada a ser criado. 
  
Alguns provedores de implementam estrita entrada verificação combinando o nome para exibição, mensagens de endereço e a chave de pesquisa em uma entrada; outros provedores de limitam a correspondência para exibir o nome e endereço. Verificação de entrada afastada geralmente é implementado, verificando o nome de exibição. 
  
## <a name="notes-to-host-address-book-provider-implementers"></a>Observações para implementadores de provedor de catálogo de endereço de Host

Se seu contêiner pode criar entradas de modelos de outros provedores, a implementação dos **CreateEntry** deverão fornecer armazenamento para algumas ou todas as propriedades associadas às entradas criadas. Por exemplo, se você fornecer armazenamento para a propriedade de **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) de uma entrada, você poderá gerar sua caixa de diálogo detalhes sem ter que dependem do provedor estrangeiro. 
  
Se seu contêiner pode criar entradas que oferecem suporte à propriedade **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)), a implementação dos **CreateEntry** deve fazer o seguinte: 
  
1. Chame o método [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) . **OpenTemplateID** permite que o código do provedor estrangeira para a entrada vincular para a nova entrada que está sendo criada. Provedores estrangeira oferecem suporte a esse processo de vinculação para manter o controle sobre entradas criados a partir de seus modelos nos contêineres de provedores de catálogo de endereço de host. 
    
2. Realizar qualquer inicialização necessária e popular o novo objeto com todas as propriedades da entrada no provedor estrangeira que o objeto retornado no parâmetro _lppMAPIPropNew_ do **OpenTemplateID**.
    
Se **OpenTemplateID** tiver êxito, copie as propriedades para a implementação apontado pelo parâmetro _lppMAPIPropNew_ e não diretamente para a implementação apontado pelo parâmetro _lpMAPIPropData_ . Inicialize a nova entrada para uso offline, como faria com qualquer outra entrada de um provedor estrangeira. 
  
Se **OpenTemplateID** retornará um erro, **CreateEntry** deve falhar. Não permita a entrada a ser criado. Como o provedor estrangeiro pode fazer suposições sobre os dados em seu provedor, não crie uma entrada com um identificador de modelo que não tenha sido associado com êxito ao provedor estrangeiro. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando **CreateEntry** retorna, você pode ou não ser capaz de acessar imediatamente o identificador de entrada para a nova entrada. Alguns provedores de catálogo de endereços não disponibilizá-lo até depois de ter chamado o método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da nova entrada. 
  
Embora os sinalizadores de verificação duplicados são passados como parâmetros para **CreateEntry**, a operação de verificação de duplicata não ocorrerá até **SaveChanges** é chamado. Portanto, os erros relacionados, como MAPI_E_COLLISION, que indica que foi feita uma tentativa para criar uma entrada já existente, são retornados pelo **SaveChanges** ao invés **CreateEntry**.
  
## <a name="see-also"></a>Confira também



[IABContainer::CopyEntries](iabcontainer-copyentries.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[Propriedade canônico de PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IABContainer: IMAPIContainer](iabcontainerimapicontainer.md)

