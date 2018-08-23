---
title: IMAPISessionSetDefaultStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.SetDefaultStore
api_type:
- COM
ms.assetid: 456c207f-5d41-4d0c-94b6-0c58893a6bed
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c7eda7089515942cb38a941bab863b3adf971bdc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587842"
---
# <a name="imapisessionsetdefaultstore"></a>IMAPISession::SetDefaultStore

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Estabelece um armazenamento de mensagens como o armazenamento de mensagens padrão para a sessão.
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla a configuração de armazenamento de mensagens padrão. Esses sinalizadores são mutuamente exclusivos; pode ser definido somente um dos sinalizadores a seguir:
    
MAPI_DEFAULT_STORE
  
> Estabelece o armazenamento de mensagens como o padrão de sessão. Atualiza a linha de tabela de status do armazenamento de mensagens, definindo o sinalizador STATUS_DEFAULT_STORE na coluna **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
MAPI_PRIMARY_STORE
  
> Estabelece o armazenamento de mensagens como o armazenamento a ser usado durante o logon. Se o armazenamento de mensagens não for o repositório padrão, os clientes devem facilitam o padrão. Atualiza a linha de tabela de status do armazenamento de mensagens, definindo o sinalizador STATUS_PRIMARY_STORE na coluna **PR_RESOURCE_FLAGS** . 
    
MAPI_SECONDARY_STORE
  
> Estabelece o armazenamento de mensagens como o armazenamento a ser usado no logon se o armazenamento de mensagens principal não estiver disponível. Se um cliente não é possível abrir o repositório principal, ele deverá abrir o armazenamento secundário e defini-la como padrão. Atualiza a linha de tabela de status do armazenamento de mensagens, definindo o sinalizador STATUS_SECONDARY_STORE na coluna **PR_RESOURCE_FLAGS** . 
    
MAPI_SIMPLE_STORE_PERMANENT
  
> Define o sinalizador STATUS_SIMPLE_STORE na propriedade **PR_RESOURCE_FLAGS** do armazenamento de mensagens em sua linha de tabela de status, linha de tabela do repositório de mensagem e em perfil da sessão. 
    
MAPI_SIMPLE_STORE_TEMPORARY
  
> Define o sinalizador STATUS_SIMPLE_STORE na propriedade **PR_RESOURCE_FLAGS** do armazenamento de mensagens em sua linha da tabela de status e a linha de tabela do repositório de mensagem. O perfil não é modificado. 
    
 _cbEntryID_
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada do repositório de mensagem que serve como o padrão. Se um cliente transmite NULL no _lpEntryID_, sem armazenamento de mensagens está selecionado como o padrão.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

O método **IMAPISession::SetDefaultStore** estabelece um armazenamento de mensagens como um destes procedimentos: 
  
- O repositório de mensagem padrão para a sessão.
    
- O repositório de mensagens principal para a sessão.
    
- O armazenamento de mensagens secundário para a sessão.
    
Para estabelecer um armazenamento de mensagens como padrão, o armazenamento de mensagens deve ter os seguintes sinalizadores definidos em sua propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)):
  
- STORE_SUBMIT_OK
    
- STORE_CREATE_OK
    
- STORE_MODIFY_OK
    
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode determinar o armazenamento de mensagens padrão para a sessão Recuperando a tabela de status e a pesquisa para que a configuração do sinalizador STATUS_DEFAULT_STORE na coluna **PR_RESOURCE_FLAGS** . Na linha que tem essa configuração representa o armazenamento de mensagens é designado como o padrão de sessão. 
  
Quando o MAPI_DEFAULT_STORE ou o sinalizador MAPI_SIMPLE_STORE_PERMANENT estiver definido, o MAPI atualiza o perfil, a tabela de repositório de mensagens e a tabela de status. 
  
Sempre que for feita uma alteração para a configuração de padrão do repositório de mensagem, as seguintes notificações são geradas:
  
- Uma notificação de evento **fnevTableModified** é emitida para cada linha afetada em ambos os tabela de status e o repositório de mensagens. 
    
- Uma notificação interna é emitida para o spooler MAPI. Operações em andamento podem ser concluídas sem alteração; novas operações que envolvem o armazenamento de mensagens padrão, como mensagem Baixando os dados, são processadas para o novo repositório padrão.
    
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnSetDefaultStore  <br/> |MFCMAPI usa o método **IMAPISession::SetDefaultStore** para definir o repositório selecionado como o armazenamento padrão.  <br/> |
   
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagResourceFlags](pidtagresourceflags-canonical-property.md)
  
[Propriedade canônica PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

