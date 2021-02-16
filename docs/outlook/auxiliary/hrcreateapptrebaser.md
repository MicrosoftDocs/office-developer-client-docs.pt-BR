---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Inicializa um objeto IOlkApptRebaser para uso em alteração da base de compromissos no calendário do Outlook.
ms.openlocfilehash: 33ad47d59ee2ca1b2461f730494f3466b9f8b54a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317609"
---
# <a name="hrcreateapptrebaser"></a>HrCreateApptRebaser

Inicializa um objeto [IOlkApptRebaser](iolkapptrebaser.md) para uso em alteração programática de compromissos em calendários do Outlook. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |tzmovelib.h  <br/> |
|Implementado por:  <br/> |tzmovelib.dll  <br/> |
|Chamado por:  <br/> |Aplicativos clientes MAPI  <br/> |
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
  
> [in] Obrigatório. Uma máscara de bits de sinalizadores usados para controlar como a alteração da base será executada. Os procedimentos sinalizadores podem ser definidos e definidos tzmovelib.h:
    
   - **REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS**, base de itens de compromisso em que o usuário é o organizador da reunião alterada. Observe que, por padrão, isso faz com que o Outlook envie atualizações da reunião aos participantes qualquer reunião que na base que está sendo alterada. Você pode combinar esse sinalizador com um **REBASE_FLAG_FORCE_NO_EX_UPDATES** ou **REBASE_FLAG_FORCE_NO_UPDATES** para alterar como são tratadas as atualizações da reunião. 
    
   - **REBASE_FLAG_UPDATE_UNMARKED**, atualizar itens de compromisso que não foram marcados com um fuso horário. Se esse sinalizador for especificado, o valor *pTZMissing* será usado como o fuso horário criado em um item para todos os itens que não têm dados fuso horário. 
    
   - **REBASE_FLAG_UPDATE_ONLYRECURRING**, atualiza os únicos itens de compromisso recorrentes. 
    
   - **REBASE_FLAG_NO_UI**, não mostram uma interface do usuário (UI), incluindo caixas de diálogo de logon geralmente exibidas ao abrir um armazenamento de mensagens. 
    
   - **REBASE_FLAG_UPDATE_MINIMIZEAPPTS** — não altera a base de itens de compromisso que ocorrem no passado. 
    
   - **REBASE_FLAG_FORCE_REBASE**, não marca o organizador para a alteração da Base de decisões, mas altera a base de itens de compromisso em que o usuário é participante. 
    
   - **REBASE_FLAG_FORCE_NO_EX_UPDATES**, envia atualizações somente se o usuário for o organizador e o destinatário e não estiver conectado a um Exchange Server. 
    
   - **REBASE_FLAG_FORCE_NO_UPDATES**, nunca enviar atualizações. 
    
   - **REBASE_FLAG_ONLY_CREATED_PRE_PATCH**, alterar a base apenas itens de compromisso criados antes da aplicação de patch. 
    
   - **REBASE_FLAG_REPORTING_MODE**, não altera a  base, apenas faz o relatório de itens de compromisso que teriam a base alterada. 
    
   - **REBASE_FLAG_SEND_RESOURCE_UPDATES**, envia atualizações da reunião para os recursos. 
    
_pSession_
  
> [in] Obrigatório. Ponteiro para uma interface de sessão MAPI.
    
_pCalendarMsgStore_
  
> [in] Obrigatório. Ponteiro para um repositório de mensagem que contém itens de compromisso para serem alterados.
    
_pCalendarFolder_
  
> [in] Obrigatório. Ponteiro para uma pasta de calendário que contém itens compromisso de para serem alterados.
    
_pwszUpdatePrefix_
  
> [in] Opcional. Ponteiro para conter o prefixo anexado em solicitações de reunião. Pode ser nulo.
    
_pftInstallDateUTC_
  
> [in] Opcional. Data da instalação o caminho do patch fuso horário. Usados somente se a **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** sinalizador estiver definido. 
    
_IExpansionDepth_
  
> [in] Opcional. A profundidade de expansão quando se está expandindo a listas de distribuição para excluir os destinatários conectados ao servidor Exchange. Usada apenas se o sinalizador **REBASE_FLAG_FORCE_NO_EX_UPDATES** sinalizador estiver definido. 
    
_pTZTo_
  
> [in] Obrigatório. Um ponteiro para uma estrutura **TZDEFINITION** descrevendo o fuso horário a ser alterado. **TZDEFINITION** definido no tzmovelib. 
    
pTZMissing
  
> [in] Obrigatório. Um ponteiro para uma estrutura **TZDEFINITION** descrevendo o fuso horário a ser considerado se as informações sobre fuso horário não estiverem marcadas em um item. Não pode ser nulo, mas somente será usado se o sinalizador **REBASE_FLAG_UPDATE_UNMARKED** estiver definido. 
    
_ppError_
  
> [out] Um ponteiro para um ponteiro para uma estrutura **MAPIERROR** contendo informações de versão, componente e informações de contexto para o erro. Pode ser nulo se nenhuma informação estendida de erro for desejada. Gratuito com [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx). 
    
_ppApptRebase_
  
> [o] Um ponteiro para um ponteiro para a interface retornada **IOlkApptRebaser**. 
    
## <a name="return-values"></a>Valor de retorno

S_OK se a chamada for bem-sucedida; caso contrário, um código de erro.
  
## <a name="remarks"></a>Comentários

Ao usar [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) para procurar o endereço dessa função em tzmovelib especifique **ApptRebaser@44** como o nome do procedimento. Nem todos os sinalizadores são válidos nas combinações entre si. 
  
Para saber mais sobre as diversas opções, confira a seção "Opções de glossário de linha de comando para a ferramenta de atualização de dados de fuso horário do Outlook " no [931667 KB: como alterar o fuso horário endereço usando a ferramenta de atualização de dados de fuso horário do Microsoft Office Outlook](https://support.microsoft.com/kb/931667/en-us).
  
## <a name="see-also"></a>Confira também

- [Sobre a alteração programática da base de calendários para o horário de verão](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

