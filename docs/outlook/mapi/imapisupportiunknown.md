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
ms.openlocfilehash: 7daa8ec536a81abc196bbb23a0e1a48e826579e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767306"
---
# <a name="imapisupport--iunknown"></a>IMAPISupport : IUnknown

  
  
**Aplica-se a**: Outlook 
  
Fornece implementações para tarefas que são normalmente executadas por provedores de serviços e funções de ponto de entrada de serviço de mensagem. Provedores de serviços de recebem um ponteiro para seu objeto de suporte ao MAPI chama o método de logon do objeto seu provedor. Serviços de mensagens recebem o ponteiro de objeto de suporte na chamada para sua função de ponto de entrada.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapispi.h  <br/> |
|Expostos pelo:  <br/> |Objetos de suporte  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços  <br/> |
|Identificador de interface:  <br/> |IID_IMAPISup  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPISUP  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[GetLastError](imapisupport-getlasterror.md) <br/> |Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro de objeto de suporte anteriores.  <br/> |
|[GetMemAllocRoutines](imapisupport-getmemallocroutines.md) <br/> |Recupera os endereços das MAPI memória alocação e desalocação funções ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)e [MAPIFreeBuffer](mapifreebuffer.md)).  <br/> |
|[Subscribe](imapisupport-subscribe.md) <br/> |Registra um coletor advise para receber notificações por meio de MAPI.  <br/> |
|[Cancelar assinatura](imapisupport-unsubscribe.md) <br/> |Cancela a responsabilidade de envio de notificações que anteriormente foi estabelecida com uma chamada para o método **Subscribe** .  <br/> |
|[Notify](imapisupport-notify.md) <br/> |Envia uma notificação de um evento especificado a uma fonte de advise originalmente registrado para a notificação por meio do método **Subscribe** .  <br/> |
|[ModifyStatusRow](imapisupport-modifystatusrow.md) <br/> |Modifica a tabela de status, adicionando uma nova linha ou modificando uma linha existente.  <br/> |
|[OpenProfileSection](imapisupport-openprofilesection.md) <br/> |Abre uma seção do perfil atual e retorna um ponteiro de [IProfSect](iprofsectimapiprop.md) para obter mais acesso  <br/> |
|[RegisterPreprocessor](imapisupport-registerpreprocessor.md) <br/> |Registra função pré-processador de um provedor de transporte (uma função que está em conformidade com o protótipo [PreprocessMessage](preprocessmessage.md) ).  <br/> |
|[NewUID](imapisupport-newuid.md) <br/> |Cria uma nova estrutura [MAPIUID](mapiuid.md) a ser usado como um identificador exclusivo.  <br/> |
|[MakeInvalid](imapisupport-makeinvalid.md) <br/> |Marca um objeto como não utilizável.  <br/> |
|[SpoolerYield](imapisupport-spooleryield.md) <br/> |Fornece o controle da CPU para o spooler MAPI para que ele pode executar qualquer tarefa que ele considera necessário.  <br/> |
|[SpoolerNotify](imapisupport-spoolernotify.md) <br/> |Notifica o MAPI spooler de uma alteração no status ou uma solicitação de serviço.  <br/> |
|[CreateOneOff](imapisupport-createoneoff.md) <br/> |Cria um identificador de entrada para um endereço one-off.  <br/> |
|[SetProviderUID](imapisupport-setprovideruid.md) <br/> |Registra uma estrutura **MAPIUID** que representa exclusivamente o provedor de serviço.  <br/> |
|[CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Compara dois identificadores de entrada para determinar se eles se referem ao mesmo objeto.  <br/> |
|[OpenTemplateID](imapisupport-opentemplateid.md) <br/> |Abre uma entrada de destinatários em um provedor de catálogo de endereço estrangeiro.  <br/> |
|[OpenEntry](imapisupport-openentry.md) <br/> |Abre um objeto e retorna um ponteiro de interface para obter mais acesso.  <br/> |
|[GetOneOffTable](imapisupport-getoneofftable.md) <br/> |Retorna um ponteiro para a tabela MAPI único (uma lista de modelos que todos no catálogo de endereços provedores de suporte para a criação de novos destinatários).  <br/> |
|[Endereço](imapisupport-address.md) <br/> |Exibe a caixa de diálogo endereço comuns.  <br/> |
|[Detalhes](imapisupport-details.md) <br/> |Exibe uma caixa de diálogo que mostra detalhes sobre uma entrada de catálogo de endereço específica.  <br/> |
|[NewEntry](imapisupport-newentry.md) <br/> |Adiciona um novo destinatário diretamente para um contêiner de catálogo de endereços ou a lista de destinatários de uma mensagem de saída.  <br/> |
|[DoConfigPropsheet](imapisupport-doconfigpropsheet.md) <br/> |Exibe uma folha de propriedades de configuração.  <br/> |
|[CopyMessages](imapisupport-copymessages.md) <br/> |Cópias ou movimentações de mensagens de uma pasta para outra pasta.  <br/> |
|[CopyFolder](imapisupport-copyfolder.md) <br/> |Copia ou move uma pasta da pasta pai atual para outra pasta pai.  <br/> |
|[DoCopyTo](imapisupport-docopyto.md) <br/> |Copia ou move todas as propriedades de um objeto, exceto propriedades especificamente excluídas, a outro objeto.  <br/> |
|[DoCopyProps](imapisupport-docopyprops.md) <br/> |Copia ou move uma ou mais propriedades de um objeto para um outro objeto.  <br/> |
|[DoProgressDialog](imapisupport-doprogressdialog.md) <br/> |Recupera um objeto de progresso que exibe um indicador de progresso.  <br/> |
|[ReadReceipt](imapisupport-readreceipt.md) <br/> |Gera uma leitura ou relatório nonread para uma mensagem.  <br/> |
|[PrepareSubmit](imapisupport-preparesubmit.md) <br/> |Prepara uma mensagem para o envio para o spooler MAPI.  <br/> |
|[ExpandRecips](imapisupport-expandrecips.md) <br/> |Conclui a lista de destinatários da mensagem, expandindo listas de distribuição particular.  <br/> |
|[DoSentMail](imapisupport-dosentmail.md) <br/> |Processa uma mensagem enviada.  <br/> |
|[OpenAddressBook](imapisupport-openaddressbook.md) <br/> |Fornece acesso ao catálogo de endereços.  <br/> |
|[CompleteMsg](imapisupport-completemsg.md) <br/> |Realiza pós-processamento em uma mensagem.  <br/> |
|[StoreLogoffTransports](imapisupport-storelogofftransports.md) <br/> |Solicita a versão ordenada de um repositório de mensagem.  <br/> |
|[StatusRecips](imapisupport-statusrecips.md) <br/> |Gera os relatórios de entrega e de não entrega.  <br/> |
|[WrapStoreEntryID](imapisupport-wrapstoreentryid.md) <br/> |Converte o identificador de entrada interna do repositório de uma mensagem para um identificador de entrada no formato padrão MAPI.  <br/> |
|[ModifyProfile](imapisupport-modifyprofile.md) <br/> |Faz com que alterações a uma mensagem armazenar seção perfil permanente.  <br/> |
|[IStorageFromStream](imapisupport-istoragefromstream.md) <br/> |Implementa um objeto de armazenamento para acessar um stream.  <br/> |
|[GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) <br/> |Cria um objeto de suporte de serviço de mensagem.  <br/> |
   
## <a name="remarks"></a>Comentários

Endereços manuais, repositórios de mensagem, provedores de transporte e mensagem serviços cada têm seus próprios objetos de suporte. Provedores de serviço e serviços de mensagem chame os métodos nos seus objetos de suporte como parte de suas implementações de outros métodos de interface. Cada objeto de suporte de diferentes tem implementações completas dos métodos que se aplicam ao seu chamador; os métodos que não são aplicáveis retornam MAPI_E_NO_SUPPORT. Objetos de suporte do provedor de catálogo de endereços têm implementações para os seguintes métodos:
  
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
   
Objetos de suporte do provedor de repositório de mensagem têm implementações para os seguintes métodos:
  
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
   
Objetos de suporte do provedor de transporte têm implementações para os seguintes métodos:
  
||||
|:-----|:-----|:-----|
|**DoConfigPropsheet** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**GetLastError** <br/> |
|**IStorageFromStream** <br/> |**MakeInvalid** <br/> |**ModifyStatusRow** <br/> |
|**OpenAddressBook** <br/> |**RegisterPreprocessor** <br/> |**NewUID** <br/> |
|**Notify** <br/> |**OpenProfileSection** <br/> |**OpenEntry** <br/> |
|**StatusRecips** <br/> |**SpoolerNotify** <br/> |**SpoolerYield** <br/> |
|**WrapStoreEntryID** <br/> |**Subscribe** <br/> |**Cancelar assinatura** <br/> |
   
Objetos de suporte de serviço de mensagem têm implementações para os seguintes métodos:
  
|||
|:-----|:-----|
|**DoConfigPropsheet** <br/> |**GetLastError** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |
|**MakeInvalid** <br/> |**NewUID** <br/> |
|**OpenProfileSection** <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

