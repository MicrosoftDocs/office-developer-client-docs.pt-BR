---
title: Copiando entradas do livro de endereços
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 285abeb4-45c8-4e82-9a16-b935b4651afe
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 190c4bf12c8f5aaaf8143f59239bb53fb68046f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418740"
---
# <a name="copying-address-book-entries"></a>Copiando entradas do livro de endereços

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O método [IABContainer::CopyEntries](iabcontainer-copyentries.md) do contêiner é chamado quando um ou mais destinatários do mesmo contêiner devem ser copiados para esse contêiner. **CopyEntries** tem quatro parâmetros de entrada: uma matriz de identificadores de entrada representando os destinatários a serem copiados, um identificador de janela para o indicador de progresso, um ponteiro de objeto de progresso e um valor de sinalizadores. Seu provedor deve exibir o progresso se o sinalizador AB_NO_DIALOG não estiver definido e usar o objeto de progresso do parâmetro  _lpProgress_ se não for NULL. Se  _lpProgress_ for NULL, chame [IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md) para usar o objeto de progresso MAPI. Para obter mais informações sobre como exibir o progresso, consulte [Exibindo um indicador de progresso.](mapi-progress-indicators.md)
  
Além de AB_NO_DIALOG para suprimir um indicador de progresso, um dos dois outros sinalizadores pode ser definido para solicitar um tipo de verificação de entrada duplicada: CREATE_CHECK_DUP_LOOSE ou CREATE_CHECK_DUP_STRICT. Os CREATE_CHECK_DUP_LOOSE e CREATE_CHECK_DUP_STRICT são apenas sugestões sobre como seu provedor determina entradas duplicadas e podem ser ignorados. MAPI suggests that your provider implement support for these flags as follows.
  
|**Sinalizador de entrada duplicado**|**Implementação sugerida**|
|:-----|:-----|
|CREATE_CHECK_DUP_LOOSE  <br/> |Verifique se o nome de exibição na entrada a ser criada corresponde ao nome de exibição de uma entrada que já está no contêiner.  <br/> |
|CREATE_CHECK_DUP_STRICT  <br/> |Verifique se o nome para exibição e a chave de pesquisa na entrada a ser criada corresponderão ao nome de exibição e à chave de pesquisa de uma entrada de contêiner.  <br/> |
   
O último sinalizador, CREATE_REPLACE, indica que a nova entrada deve substituir a existente se o provedor tiver determinado que uma entrada a ser criada é uma duplicata de uma entrada que já está no contêiner. 
  
Se seu provedor for um livro de endereços **pessoal,** inclua a propriedade PR_DETAILS_TABLE ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) em cada operação de cópia. Incluir a tabela de exibição de detalhes de um destinatário copiado permite que seu contêiner exibir os detalhes do destinatário em vez de ter que chamar o contêiner original para criar a exibição.
  
 **Para implementar IABContainer::CopyEntries**
  
1. Determine se cada identificador de entrada no parâmetro  _lpEntries_ está em um formato que seu provedor trata e, se não estiver, falhar e retornar MAPI_E_INVALID_ENTRYID. 
    
2. Se um identificador de entrada representar um usuário de mensagens, uma lista de distribuição ou um contêiner que seu provedor manipulará:
    
1. Chame seu [método IMAPISupport::OpenEntry](imapisupport-openentry.md) para abrir o destinatário correspondente. 
    
2. Copie o destinatário para o contêiner. 
    
3. Se o identificador de entrada representar um destinatário estrangeiro:
    
1. Chame o método [IABContainer::CreateEntry](iabcontainer-createentry.md) do contêiner para criar um novo destinatário. 
    
2. Definir propriedades iniciais no novo destinatário.
    
4. Chame o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) do novo objeto para salvá-lo. 
    
5. Atualize a tabela de conteúdo do contêiner para refletir o novo destinatário. 
    
6. Chame [IMAPISupport::Notify](imapisupport-notify.md) para enviar uma notificação de tabela para clientes registrados. 
    

