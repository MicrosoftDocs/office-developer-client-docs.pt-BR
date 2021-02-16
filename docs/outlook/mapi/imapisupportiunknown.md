---
title: IMAPISupport IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport
api_type:
- COM
ms.assetid: 92bfe604-18dd-46a1-9ae8-0b04167606bd
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6da488408d3be9464d6ae1e016d5095707d451e4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415436"
---
# <a name="imapisupport--iunknown"></a>IMAPISupport : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece implementações para tarefas que normalmente são executadas por provedores de serviços e funções de ponto de entrada do serviço de mensagens. Os provedores de serviços recebem um ponteiro para seu objeto de suporte quando o MAPI chama o método de logon do objeto do provedor. Os serviços de mensagens recebem o ponteiro do objeto de suporte na chamada para sua função de ponto de entrada.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapispi.h  <br/> |
|Exposto por:  <br/> |Objetos de suporte  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Provedores de serviços  <br/> |
|Identificador de interface:  <br/> |IID_IMAPISup  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPISUP  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[GetLastError](imapisupport-getlasterror.md) <br/> |Retorna uma [estrutura MAPIERROR](mapierror.md) que contém informações sobre o erro de objeto de suporte anterior.  <br/> |
|[GetMemAllocRoutines](imapisupport-getmemallocroutines.md) <br/> |Recupera os endereços das funções de alocação e alocação de memória MAPI ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)e [MAPIFreeBuffer](mapifreebuffer.md)).  <br/> |
|[Subscribe](imapisupport-subscribe.md) <br/> |Registra um evento de aviso para receber notificações por meio de MAPI.  <br/> |
|[Cancelar assinatura](imapisupport-unsubscribe.md) <br/> |Cancela a responsabilidade de enviar notificações que foram estabelecidas anteriormente com uma chamada para o **método Subscribe.**  <br/> |
|[Notify](imapisupport-notify.md) <br/> |Envia uma notificação de um evento especificado para uma fonte de aviso que originalmente registrada para a notificação por meio do **método Subscribe.**  <br/> |
|[ModifyStatusRow](imapisupport-modifystatusrow.md) <br/> |Modifica a tabela de status adicionando uma nova linha ou modificando uma linha existente.  <br/> |
|[OpenProfileSection](imapisupport-openprofilesection.md) <br/> |Abre uma seção do perfil atual e retorna um ponteiro [IProfSect](iprofsectimapiprop.md) para mais acesso  <br/> |
|[RegisterPreprocessor](imapisupport-registerpreprocessor.md) <br/> |Registra a função de pré-processador de um provedor de transporte (uma função que está em conformidade com o protótipo [PreprocessMessage).](preprocessmessage.md)  <br/> |
|[NewUID](imapisupport-newuid.md) <br/> |Cria uma nova [estrutura MAPIUID](mapiuid.md) a ser usada como um identificador exclusivo.  <br/> |
|[MakeInvalid](imapisupport-makeinvalid.md) <br/> |Marca um objeto como inutilizável.  <br/> |
|[SpoolerYield](imapisupport-spooleryield.md) <br/> |Fornece controle da CPU para o spooler MAPI para que ele possa executar todas as tarefas que considera necessárias.  <br/> |
|[SpoolerNotify](imapisupport-spoolernotify.md) <br/> |Notifica o spooler MAPI sobre uma alteração no status ou uma solicitação de serviço.  <br/> |
|[CreateOneOff](imapisupport-createoneoff.md) <br/> |Cria um identificador de entrada para um endereço único.  <br/> |
|[SetProviderUID](imapisupport-setprovideruid.md) <br/> |Registra uma estrutura **MAPIUID** que representa exclusivamente o provedor de serviços.  <br/> |
|[CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Compara dois identificadores de entrada para determinar se eles se referem ao mesmo objeto.  <br/> |
|[OpenTemplateID](imapisupport-opentemplateid.md) <br/> |Abre uma entrada de destinatário em um provedor de agendas externas.  <br/> |
|[OpenEntry](imapisupport-openentry.md) <br/> |Abre um objeto e retorna um ponteiro de interface para mais acesso.  <br/> |
|[GetOneOffTable](imapisupport-getoneofftable.md) <br/> |Retorna um ponteiro para a tabela única MAPI (uma lista de modelos que todos os provedores de agenda de endereços suportam para criar novos destinatários).  <br/> |
|[Endereço](imapisupport-address.md) <br/> |Exibe a caixa de diálogo de endereço comum.  <br/> |
|[Detalhes](imapisupport-details.md) <br/> |Exibe uma caixa de diálogo que mostra detalhes sobre uma entrada específica do livro de endereços.  <br/> |
|[NewEntry](imapisupport-newentry.md) <br/> |Adiciona um novo destinatário diretamente a um contêiner de livro de endereços ou à lista de destinatários de uma mensagem de saída.  <br/> |
|[DoConfigPropsheet](imapisupport-doconfigpropsheet.md) <br/> |Exibe uma folha de propriedades de configuração.  <br/> |
|[CopyMessages](imapisupport-copymessages.md) <br/> |Copia ou move mensagens de uma pasta para outra.  <br/> |
|[CopyFolder](imapisupport-copyfolder.md) <br/> |Copia ou move uma pasta de sua pasta pai atual para outra pasta pai.  <br/> |
|[DoCopyTo](imapisupport-docopyto.md) <br/> |Copia ou move todas as propriedades de um objeto, exceto para propriedades especificamente excluídas, para outro objeto.  <br/> |
|[DoCopyProps](imapisupport-docopyprops.md) <br/> |Copia ou move uma ou mais propriedades de um objeto para outro objeto.  <br/> |
|[DoProgressDialog](imapisupport-doprogressdialog.md) <br/> |Recupera um objeto de progresso que exibe um indicador de progresso.  <br/> |
|[ReadReceipt](imapisupport-readreceipt.md) <br/> |Gera um relatório lido ou não lido para uma mensagem.  <br/> |
|[PrepareSubmit](imapisupport-preparesubmit.md) <br/> |Prepara uma mensagem para envio ao spooler MAPI.  <br/> |
|[ExpandRecips](imapisupport-expandrecips.md) <br/> |Conclui a lista de destinatários de uma mensagem, expandindo listas de distribuição específicas.  <br/> |
|[DoSentMail](imapisupport-dosentmail.md) <br/> |Processa uma mensagem enviada.  <br/> |
|[OpenAddressBook](imapisupport-openaddressbook.md) <br/> |Fornece acesso ao livro de endereços.  <br/> |
|[CompleteMsg](imapisupport-completemsg.md) <br/> |Executa pós-processamento em uma mensagem.  <br/> |
|[StoreLogoffTransports](imapisupport-storelogofftransports.md) <br/> |Solicita a liberação pedido de um armazenamento de mensagens.  <br/> |
|[StatusRecips](imapisupport-statusrecips.md) <br/> |Gera relatórios de entrega e não entrega.  <br/> |
|[WrapStoreEntryID](imapisupport-wrapstoreentryid.md) <br/> |Converte o identificador de entrada interno de um armazenamento de mensagens em um identificador de entrada no formato padrão MAPI.  <br/> |
|[ModifyProfile](imapisupport-modifyprofile.md) <br/> |Faz alterações em uma seção de perfil de armazenamento de mensagens permanente.  <br/> |
|[IStorageFromStream](imapisupport-istoragefromstream.md) <br/> |Implementa um objeto de armazenamento para acessar um fluxo.  <br/> |
|[GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) <br/> |Cria um objeto de suporte do serviço de mensagens.  <br/> |
   
## <a name="remarks"></a>Comentários

Os address books, os armazenamentos de mensagens, os provedores de transporte e os serviços de mensagens têm seus próprios objetos de suporte. Provedores de serviços e serviços de mensagens chamam os métodos em seus objetos de suporte como parte de suas implementações de outros métodos de interface. Cada objeto de suporte diferente tem implementações completas dos métodos que se aplicam ao seu chamador; os métodos que não são aplicáveis retornam MAPI_E_NO_SUPPORT. Os objetos de suporte do provedor de agendas têm implementações para os seguintes métodos:
  
||||
|:-----|:-----|:-----|
|**Endereço** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**Detalhes** <br/> |**DoConfigPropsheet** <br/> |**DoProgressDialog** <br/> |
|**GetLastError** <br/> |**GetMemAllocRoutines** <br/> |**GetOneOffTable** <br/> |
|**IStorageFromStream** <br/> |**GetSvcConfigSupportObj** <br/> |**MakeInvalid** <br/> |
|**ModifyStatusRow** <br/> |**NewEntry** <br/> |**NewUID** <br/> |
|**Notify** <br/> |**OpenAddressBook** <br/> |**OpenEntry** <br/> |
|**OpenProfileSection** <br/> |**OpenTemplateID** <br/> |**SetProviderUID** <br/> |
|**Subscribe** <br/> |**Cancelar assinatura** <br/> |**WrapStoreEntryID** <br/> |
   
Os objetos de suporte do provedor de armazenamento de mensagens têm implementações para os seguintes métodos:
  
||||
|:-----|:-----|:-----|
|**CompareEntryIDs** <br/> |**CompleteMsg** <br/> |**CopyFolder** <br/> |
|**CopyMessages** <br/> |**CreateOneOff** <br/> |**DoCopyProps** <br/> |
|**DoCopyTo** <br/> |**DoConfigPropsheet** <br/> |**DoProgressDialog** <br/> |
|**DoSentMail** <br/> |**ExpandRecips** <br/> |**GetLastError** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**MakeInvalid** <br/> |
|**IStorageFromStream** <br/> |**ModifyProfile** <br/> |**ModifyStatusRow** <br/> |
|**NewUID** <br/> |**Notify** <br/> |**OpenAddressBook** <br/> |
|**OpenEntry** <br/> |**OpenProfileSection** <br/> |**PrepareSubmit** <br/> |
|**ReadReceipt** <br/> |**SetProviderUID** <br/> |**SpoolerNotify** <br/> |
|**StoreLogoffTransports** <br/> |**Subscribe** <br/> |**Cancelar assinatura** <br/> |
|**WrapStoreEntryID** <br/> |
   
Os objetos de suporte do provedor de transporte têm implementações para os seguintes métodos:
  
||||
|:-----|:-----|:-----|
|**DoConfigPropsheet** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**GetLastError** <br/> |
|**IStorageFromStream** <br/> |**MakeInvalid** <br/> |**ModifyStatusRow** <br/> |
|**OpenAddressBook** <br/> |**RegisterPreprocessor** <br/> |**NewUID** <br/> |
|**Notify** <br/> |**OpenProfileSection** <br/> |**OpenEntry** <br/> |
|**StatusRecips** <br/> |**SpoolerNotify** <br/> |**SpoolerYield** <br/> |
|**WrapStoreEntryID** <br/> |**Subscribe** <br/> |**Cancelar assinatura** <br/> |
   
Os objetos de suporte do serviço de mensagens têm implementações para os seguintes métodos:
  
|||
|:-----|:-----|
|**DoConfigPropsheet** <br/> |**GetLastError** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |
|**MakeInvalid** <br/> |**NewUID** <br/> |
|**OpenProfileSection** <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

