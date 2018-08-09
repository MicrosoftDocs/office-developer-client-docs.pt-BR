---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Inicializa um objeto IOlkApptRebaser para uso na alteração da base compromissos no calendário do Outlook.
ms.openlocfilehash: fec0407c3f129290d03f9b26b0b3f072a229b003
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765822"
---
# <a name="hrcreateapptrebaser"></a>HrCreateApptRebaser

Inicializa um objeto [IOlkApptRebaser](iolkapptrebaser.md) para uso na alteração da base compromissos no calendário do Outlook. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |tzmovelib.h  <br/> |
|Implementada por:  <br/> |tzmovelib.dll  <br/> |
|Chamado pelo:  <br/> |Aplicativos de cliente MAPI  <br/> |
|Tipo de ponteiro:  <br/> |**LPHRCREATEAPPTREBASER** <br/> |
|Ponto de entrada DLL:  <br/> |**HrCreateApptRebaser@44** <br/> |
   
```cpp
HRESULT HrCreateApptRebaser(  
    ULONG ulFlags, 
    IMAPISession *pSession, 
    IMsgStore *pCalendarMsgStore, 
    IMAPIFolder *pCalendarFolder, 
    LPCWSTR pwszUpdatePrefix, 
    const FILETIME *pftInstallDateUTC, 
    LONG lExpansionDepth, 
    const TZDEFINITION *pTZTo, 
    const TZDEFINITION *pTZMissing, 
    MAPIERROR **ppError, 
    IOlkApptRebaser **ppApptRebase); 

```

## <a name="parameters"></a>Parâmetros

_ulFlags_
  
> [in] Necessário. Uma bitmask dos sinalizadores usados para controlar como a alteração da base é executada. Sinalizadores a seguir podem ser definidos e definidos no tzmovelib.h:
    
   - **REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** — os itens de compromisso em que o usuário é o organizador da reunião são base alterados. Observe que, por padrão, isso faz com que o Outlook enviar atualizações de reunião para todos os participantes de qualquer reunião a base que está sendo alterada. Você pode combinar esse sinalizador com **REBASE_FLAG_FORCE_NO_EX_UPDATES** ou **REBASE_FLAG_FORCE_NO_UPDATES** para alterar como as atualizações de reunião são manipuladas. 
    
   - **REBASE_FLAG_UPDATE_UNMARKED** — atualizar itens de compromisso que não foram marcados com um fuso horário. Se esse sinalizador for especificado, o valor de *pTZMissing* é usado como o fuso horário que um item é criado em todos os itens que não têm dados de fuso horário. 
    
   - **REBASE_FLAG_UPDATE_ONLYRECURRING** — atualizar apenas itens de compromisso recorrente. 
    
   - **REBASE_FLAG_NO_UI** — não mostrar nenhuma interface de usuário (UI), incluindo caixas de diálogo de logon geralmente exibidas ao abrir um armazenamento de mensagens. 
    
   - **REBASE_FLAG_UPDATE_MINIMIZEAPPTS** — não alterar a base de itens de compromisso que ocorrem no passado. 
    
   - **REBASE_FLAG_FORCE_REBASE** — não verificar o organizador para a alteração da Base de decisões, mas alterar a base de itens de compromisso em que o usuário é um participante. 
    
   - **REBASE_FLAG_FORCE_NO_EX_UPDATES** — envia as atualizações somente se o usuário é o organizador e o destinatário não está conectado a um servidor Exchange. 
    
   - **REBASE_FLAG_FORCE_NO_UPDATES** — nunca enviar atualizações. 
    
   - **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** — alterar a base apenas os itens de compromisso de ocorrência única criados antes da aplicação do patch. 
    
   - **REBASE_FLAG_REPORTING_MODE** — fazer na verdade não alterar, a base do relatório apenas itens de compromisso que seria ser alterado. 
    
   - **REBASE_FLAG_SEND_RESOURCE_UPDATES** — enviar atualizações de reunião para os recursos. 
    
_pSession_
  
> [in] Necessário. Um ponteiro para uma interface de sessão MAPI.
    
_pCalendarMsgStore_
  
> [in] Necessário. Um ponteiro para um armazenamento de mensagens que contêm os itens de compromisso de ser alterada.
    
_pCalendarFolder_
  
> [in] Necessário. Um ponteiro para uma pasta de calendário que contém itens de compromisso de ser alterada.
    
_pwszUpdatePrefix_
  
> [in] Opcional. Um ponteiro para uma cadeia de caracteres que contém o prefixo a serem anexados em solicitações de reunião. Pode ser NULL.
    
_pftInstallDateUTC_
  
> [in] Opcional. Data da instalação do patch de fuso horário. Usado somente se o sinalizador **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** está definido. 
    
_IExpansionDepth_
  
> [in] Opcional. A profundidade de expansão quando Expandindo listas de distribuição para excluir os destinatários conectados ao servidor do Exchange. Usado somente se o sinalizador **REBASE_FLAG_FORCE_NO_EX_UPDATES** está definido. 
    
_pTZTo_
  
> [in] Necessário. Um ponteiro para uma estrutura **TZDEFINITION** descrevendo o fuso horário de ser alterada para. **TZDEFINITION** é definido em tzmovelib. 
    
pTZMissing
  
> [in] Necessário. Um ponteiro para uma estrutura **TZDEFINITION** descrevendo o fuso horário para ser assumido se as informações de fuso horário não estiver marcadas em um item. Não deve ser nulo, mas somente usado se o sinalizador **REBASE_FLAG_UPDATE_UNMARKED** está definido. 
    
_ppError_
  
> [out] Um ponteiro para um ponteiro para uma estrutura **MAPIERROR** contendo informações de versão, componente e contexto para o erro. Pode ser NULL se não há informações de erro estendidas for desejadas. Livre com [MAPIFreeBuffer](http://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx). 
    
_ppApptRebase_
  
> [out] Um ponteiro para um ponteiro para a interface **IOlkApptRebaser** retornado. 
    
## <a name="return-values"></a>Valores de retorno

S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.
  
## <a name="remarks"></a>Comentários

Ao usar o [GetProcAddress](http://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) para procurar o endereço desta função no tzmovelib.dll, especifique **HrCreateApptRebaser@44** como o nome do procedimento. Nem todos os sinalizadores são válidos em combinação com umas às outras. 
  
Para obter mais informações sobre as várias opções, consulte a seção "Glossário de opções de linha de comando da ferramenta de atualização de dados de fuso horário do Outlook" em [KB 931667: alterações de fuso horário do endereço, usando a ferramenta de atualização de dados de fuso horário para Microsoft Office Outlook como](http://support.microsoft.com/kb/931667/en-us).
  
## <a name="see-also"></a>Confira também

- [Sobre alteração de calendários por meio de programação para horário de verão](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

