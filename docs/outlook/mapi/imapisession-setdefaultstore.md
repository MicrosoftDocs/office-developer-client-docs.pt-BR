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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335801"
---
# <a name="imapisessionsetdefaultstore"></a>IMAPISession::SetDefaultStore

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Estabelece um repositório de mensagens como o repositório de mensagens padrão para a sessão.
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla a configuração do repositório de mensagens padrão. Esses sinalizadores são mutuamente exclusivos; apenas um dos seguintes sinalizadores pode ser definido:
    
MAPI_DEFAULT_STORE
  
> Estabelece o repositório de mensagens como o padrão da sessão. Atualiza a linha da tabela de status do repositório de mensagens definindo o sinalizador STATUS_DEFAULT_STORE na coluna **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
MAPI_PRIMARY_STORE
  
> Estabelece o repositório de mensagens como o repositório a ser usado no logon. Se o repositório de mensagens não for o repositório padrão, os clientes devem torná-lo o padrão. Atualiza a linha da tabela de status do repositório de mensagens definindo o sinalizador STATUS_PRIMARY_STORE na coluna **PR_RESOURCE_FLAGS** . 
    
MAPI_SECONDARY_STORE
  
> Estabelece o repositório de mensagens como o repositório a ser usado no logon se o repositório de mensagens principal não estiver disponível. Se um cliente não puder abrir o armazenamento principal, ele deverá abrir o repositório secundário e defini-lo como o padrão. Atualiza a linha da tabela de status do repositório de mensagens definindo o sinalizador STATUS_SECONDARY_STORE na coluna **PR_RESOURCE_FLAGS** . 
    
MAPI_SIMPLE_STORE_PERMANENT
  
> Define o sinalizador STATUS_SIMPLE_STORE na propriedade **PR_RESOURCE_FLAGS** do repositório de mensagens em sua linha da tabela de status, linha da tabela de repositórios de mensagens e no perfil da sessão. 
    
MAPI_SIMPLE_STORE_TEMPORARY
  
> Define o sinalizador STATUS_SIMPLE_STORE na propriedade **PR_RESOURCE_FLAGS** do armazenamento de mensagens em sua linha da tabela de linha e repositório de mensagens da tabela de status. O perfil não é modificado. 
    
 _cbEntryID_
  
> no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> no Um ponteiro para o identificador de entrada do repositório de mensagens destinado como o padrão. Se um cliente passa nulo no _lpEntryID_, nenhum repositório de mensagens é selecionado como o padrão.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

O método **IMAPISession:: SetDefaultStore** estabelece um repositório de mensagens como um dos seguintes: 
  
- O repositório de mensagens padrão da sessão.
    
- O repositório de mensagens principal da sessão.
    
- O repositório de mensagens secundário da sessão.
    
Para estabelecer um repositório de mensagens como o padrão, o repositório de mensagens deve ter os seguintes sinalizadores definidos em sua propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)):
  
- STORE_SUBMIT_OK
    
- STORE_CREATE_OK
    
- STORE_MODIFY_OK
    
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode determinar o repositório de mensagens padrão para a sessão, recuperando a tabela de status e procurando a configuração do sinalizador STATUS_DEFAULT_STORE na coluna **PR_RESOURCE_FLAGS** . A linha que tem essa configuração representa o repositório de mensagens designado como o padrão da sessão. 
  
Quando o sinalizador MAPI_DEFAULT_STORE ou MAPI_SIMPLE_STORE_PERMANENT está definido, o MAPI atualiza o perfil, a tabela do repositório de mensagens e a tabela de status. 
  
Sempre que uma alteração é feita na configuração padrão do repositório de mensagens, as seguintes notificações são geradas:
  
- Uma notificação de evento **fnevTableModified** é emitida para cada linha afetada no repositório de mensagens e na tabela de status. 
    
- Uma notificação interna é emitida para o spooler MAPI. As operações já em andamento são concluídas sem alterações; novas operações que envolvem o repositório de mensagens padrão, como download de mensagens, são processadas para o novo repositório padrão.
    
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MainDlg. cpp  <br/> |CMainDlg:: OnSetDefaultStore  <br/> |MFCMAPI usa o método **IMAPISession:: SetDefaultStore** para definir o repositório selecionado como o repositório padrão.  <br/> |
   
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagResourceFlags](pidtagresourceflags-canonical-property.md)
  
[Propriedade canônica PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

