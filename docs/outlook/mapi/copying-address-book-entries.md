---
title: Copiar entradas do catálogo de endereços
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 285abeb4-45c8-4e82-9a16-b935b4651afe
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: eca0c9f63a4efaaa7f9fd066cf5dce451b8f6175
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565883"
---
# <a name="copying-address-book-entries"></a>Copiar entradas do catálogo de endereços

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Método de [IABContainer::CopyEntries](iabcontainer-copyentries.md) do seu contêiner é chamado quando um ou mais destinatários no mesmo ou outro contêiner devem ser copiados para este contêiner. **CopyEntries** tem quatro parâmetros de entrada: uma matriz de identificadores de entrada que representa os destinatários a serem copiados, um identificador de janela para o indicador de progresso, um indicador de progresso do objeto e um valor de flags. Seu provedor deve exibir o progresso, se o sinalizador AB_NO_DIALOG não estiver definido e use o objeto de progresso do parâmetro _lpProgress_ se não for nula. Se _lpProgress_ for NULL, chame [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) para usar o objeto de progresso MAPI. Para obter mais informações sobre como exibir o progresso, consulte [exibindo um indicador de progresso](mapi-progress-indicators.md).
  
Além das AB_NO_DIALOG suprimir um indicador de progresso, um dos dois outros sinalizadores pode ser definido como solicitar um tipo de verificação de entrada duplicada: CREATE_CHECK_DUP_LOOSE ou CREATE_CHECK_DUP_STRICT. Os sinalizadores CREATE_CHECK_DUP_LOOSE e CREATE_CHECK_DUP_STRICT são apenas sugestões sobre como o seu provedor determina entradas duplicadas e podem ser ignorados. MAPI sugere que seu provedor de implementar o suporte para esses sinalizadores da seguinte maneira.
  
|**Sinalizador de entrada duplicada**|**Implementação sugerida**|
|:-----|:-----|
|CREATE_CHECK_DUP_LOOSE  <br/> |Verifique se o nome de exibição na entrada a ser criado corresponde ao nome de exibição de uma entrada já no contêiner.  <br/> |
|CREATE_CHECK_DUP_STRICT  <br/> |Verifique se o nome de exibição e a chave de pesquisa na entrada a ser criado correspondem à chave de nome e a pesquisa de exibição de uma entrada de contêiner.  <br/> |
   
O último sinalizador, CREATE_REPLACE, indica que a nova entrada deve substituir o já existente, se seu provedor determinou que uma entrada a ser criado é uma duplicata de uma entrada já em seu contêiner. 
  
Se seu provedor for um catálogo particular de endereços, inclua a propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) em cada operação de cópia. Incluindo a tabela de exibição de detalhes de um destinatário copiada permite seu contêiner exibir os detalhes de destinatário em vez de entrar em contato com o contêiner original para criar a exibição.
  
 **Para implementar IABContainer::CopyEntries**
  
1. Determine se cada identificador de entrada no parâmetro _lpEntries_ está em um formato que seu provedor manipula e se não estiver, falhar e retornar MAPI_E_INVALID_ENTRYID. 
    
2. Se um identificador de entrada representa um usuário de mensagens, lista de distribuição ou contêiner que lida com o seu provedor:
    
1. Chame o método [IMAPISupport::OpenEntry](imapisupport-openentry.md) para abrir o destinatário correspondente. 
    
2. Copie o destinatário para o seu contêiner. 
    
3. Se o identificador de entrada representa um destinatário externo:
    
1. Chame o método de [IABContainer::CreateEntry](iabcontainer-createentry.md) do seu contêiner para criar um novo destinatário. 
    
2. Definir propriedades iniciais sobre o novo destinatário.
    
4. Chame o novo método do objeto [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para salvá-la. 
    
5. Atualize a tabela de conteúdo do contêiner para refletir o novo destinatário. 
    
6. Chame [IMAPISupport::Notify](imapisupport-notify.md) para enviar uma notificação de tabela para os clientes registrados. 
    

