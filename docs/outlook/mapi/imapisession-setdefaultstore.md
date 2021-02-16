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
ms.openlocfilehash: f4ff2a3897306ebe4f77c08630782c5f2c7d5d3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426104"
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
  
> [in] Uma máscara de bits de sinalizadores que controla a configuração do armazenamento de mensagens padrão. Esses sinalizadores são mutuamente exclusivos; somente um dos sinalizadores a seguir pode ser definido:
    
MAPI_DEFAULT_STORE
  
> Estabelece o armazenamento de mensagens como o padrão da sessão. Atualiza a linha da tabela de status do armazenamento de mensagens definindo o sinalizador STATUS_DEFAULT_STORE na coluna **PR_RESOURCE_FLAGS** ([PidTagResourceFlags).](pidtagresourceflags-canonical-property.md)
    
MAPI_PRIMARY_STORE
  
> Estabelece o armazenamento de mensagens como o armazenamento a ser usado no logon. Se o armazenamento de mensagens não for o armazenamento padrão, os clientes deverão torná-lo o padrão. Atualiza a linha da tabela de status do armazenamento de mensagens definindo o sinalizador STATUS_PRIMARY_STORE na **PR_RESOURCE_FLAGS** coluna. 
    
MAPI_SECONDARY_STORE
  
> Estabelece o armazenamento de mensagens como o armazenamento a ser usado no logon se o armazenamento de mensagens principal não estiver disponível. Se um cliente não puder abrir o armazenamento principal, ele deverá abrir o armazenamento secundário e defini-lo como padrão. Atualiza a linha da tabela de status do armazenamento de mensagens definindo o sinalizador STATUS_SECONDARY_STORE na **PR_RESOURCE_FLAGS** coluna. 
    
MAPI_SIMPLE_STORE_PERMANENT
  
> Define o STATUS_SIMPLE_STORE sinalizador de erro na propriedade **PR_RESOURCE_FLAGS** do armazenamento de mensagens na linha da tabela de status, na linha da tabela do armazenamento de mensagens e no perfil da sessão. 
    
MAPI_SIMPLE_STORE_TEMPORARY
  
> Define o STATUS_SIMPLE_STORE sinalizador de erro  na propriedade PR_RESOURCE_FLAGS do armazenamento de mensagens na linha da tabela de status e na linha da tabela do armazenamento de mensagens. O perfil não é modificado. 
    
 _cbEntryID_
  
> [in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada do armazenamento de mensagens que se destina como padrão. Se um cliente passar NULL em  _lpEntryID_, nenhum armazenamento de mensagens será selecionado como padrão.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

O **método IMAPISession::SetDefaultStore** estabelece um repositório de mensagens como um dos seguintes: 
  
- O armazenamento de mensagens padrão da sessão.
    
- O armazenamento de mensagens principal da sessão.
    
- O armazenamento secundário de mensagens da sessão.
    
Para estabelecer um repositório de mensagens como padrão, o repositório de mensagens deve ter os seguintes sinalizadores definidos em sua **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) propriedade:
  
- STORE_SUBMIT_OK
    
- STORE_CREATE_OK
    
- STORE_MODIFY_OK
    
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode determinar o armazenamento de mensagens padrão para a sessão recuperando a tabela de status e procurando a configuração do sinalizador STATUS_DEFAULT_STORE na **PR_RESOURCE_FLAGS** coluna. A linha que tem essa configuração representa o armazenamento de mensagens designado como o padrão de sessão. 
  
Quando o MAPI_DEFAULT_STORE ou o sinalizador MAPI_SIMPLE_STORE_PERMANENT está definido, o MAPI atualiza o perfil, a tabela de armazenamento de mensagens e a tabela de status. 
  
Sempre que uma alteração é feita na configuração padrão do armazenamento de mensagens, as seguintes notificações são geradas:
  
- Uma **notificação de evento fnevTableModified** é emitida para cada linha afetada no armazenamento de mensagens e na tabela de status. 
    
- Uma notificação interna é emitida para o spooler MAPI. As operações já em andamento são concluídas sem alteração; novas operações que envolvem o armazenamento de mensagens padrão, como o download de mensagens, são processadas para o novo armazenamento padrão.
    
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnSetDefaultStore  <br/> |MFCMAPI usa o **método IMAPISession::SetDefaultStore** para definir o repositório selecionado como o repositório padrão.  <br/> |
   
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagResourceFlags](pidtagresourceflags-canonical-property.md)
  
[Propriedade canônica PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

