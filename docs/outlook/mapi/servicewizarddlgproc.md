---
title: SERVICEWIZARDDLGPROC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SERVICEWIZARDDLGPROC
api_type:
- COM
ms.assetid: 3e2d5190-e67a-470d-8177-0f0ba20c7b82
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e43a1d7c57668ba930b4c4af7194bd298971e6ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432377"
---
# <a name="servicewizarddlgproc"></a>SERVICEWIZARDDLGPROC
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define uma função de retorno de chamada invocada pelo assistente de perfil para permitir que um provedor de serviços reagir a eventos do usuário quando as folhas de propriedades ou páginas do provedor estiverem sendo mostradas. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiwz. h  <br/> |
|Função definida implementada por:  <br/> |Provedores de serviços  <br/> |
|Função definida chamada por:  <br/> |Assistente de perfil MAPI  <br/> |
   
```cpp
BOOL SERVICEWIZARDDLGPROC(
  HWND hDlg,
  UINT wMsgID,
  WPARAM wParam,
  LPARAM lParam
);
```

## <a name="parameters"></a>Parâmetros

_hDlg_
  
> no Manipulador de janela para a caixa de diálogo Assistente de perfil. 
    
_wMsgID_
  
> no A mensagem da janela a ser processada. Além das mensagens de janela regulares esperadas por uma caixa de diálogo modal, as seguintes mensagens podem ser recebidas:
    
WM_CLOSE 
  
> O assistente de perfil foi concluído. O provedor de serviços deve fazer todas as limpezas necessárias, como desalocar qualquer memória alocada dinamicamente. 
    
WM_COMMAND 
  
> Um dos controles do provedor foi selecionado ou o botão **Avançar** ou **voltar** foi clicado. O valor no parâmetro _wParam_ indica qual desses eventos de usuário ocorreu. 
    
WM_INITDIALOG 
  
> O usuário foi movido para outra página de propriedades, para a qual a caixa de diálogo deve ser inicializada. O provedor deve inicializar os controles que o assistente de perfil adicionou à caixa de diálogo. 
    
WIZ_QUERYNUMPAGES 
  
> O assistente de perfil está solicitando o número de páginas que o provedor precisa exibir. O provedor deve retornar o número de páginas em vez de TRUE ou FALSE. Por exemplo, use a seguinte instrução de retorno para indicar que três páginas devem ser exibidas:
    
   ```cpp
return (BOOL)3;

   ```

_wParam_
  
> no Um parâmetro de 32 bits associado a mensagens de janela. Os valores possíveis dependem da mensagem especificada no parâmetro _wMsgID_ . Além dos valores esperados com as mensagens de janela regulares de uma caixa de diálogo modal, os seguintes valores podem ser recebidos: 
    
WIZ_NEXT 
  
> Quando _wMsgID_ contiver WM_COMMAND, o usuário clicou no botão **Avançar** . 
    
WIZ_PREV 
  
> Quando _wMsgID_ contiver WM_COMMAND, o usuário clicou no botão **voltar** . 
    
_lParam_
  
> no Um parâmetro de 32 bits associado a mensagens de janela. Os valores possíveis dependem da mensagem especificada no parâmetro _wMsgID_ . 
    
## <a name="return-value"></a>Valor de retorno

O valor retornado por uma função baseada em **SERVICEWIZARDDLGPROC** depende da mensagem de janela recebida. Observe em particular o valor de retorno excepcional para a mensagem WIZ_QUERYNUMPAGES. Os valores de retorno normais são: 
  
TRUE 
  
> O provedor de serviços processou a mensagem de janela recebida. 
    
FALSE 
  
> O provedor de serviços não processou a mensagem de janela recebida.
    
## <a name="remarks"></a>Comentários

Quando o usuário move de uma página de propriedades para outra, o provedor é responsável por ocultar os controles da página antiga e mostrar os controles da página seguinte ou anterior. Quando o usuário clica no botão **Avançar** , a função baseada em **SERVICEWIZARDDLGPROC** é chamada com a mensagem WM_COMMAND e WIZ_NEXT no parâmetro _wParam_ . As etapas a seguir descrevem o que ocorre entre o momento em que o usuário clica **em Avançar** e a hora em que as páginas de configuração do primeiro provedor são renderizadas. 
  
1. O assistente de perfil oculta os controles que estão na janela. 
    
2. O assistente de perfil adiciona os controles ocultos do provedor à página. 
    
3. O assistente de perfil chama **SERVICEWIZARDDLGPROC**, enviando a mensagem WM_INITDIALOG, para que o provedor possa inicializar os controles. 
    
4. O assistente de perfil chama **SERVICEWIZARDDLGPROC**, enviando a mensagem WIZ_QUERYNUMPAGES. O provedor retorna o número de páginas que devem ser mostradas. 
    
5. O assistente de perfil chama **SERVICEWIZARDDLGPROC**, enviando a mensagem WM_COMMAND com o parâmetro _wParam_ definido como WIZ_NEXT ou WIZ_PREV. Neste ponto, o provedor retorna FALSE {erro} ou revela seus controles e retorna TRUE {Success}. Se o assistente de perfil passar no ID_NEXT, a primeira página do provedor será exibida. Se ID_PREV for passado, a última página é exibida. 
    
6. O assistente de perfil chama a função **SERVICEWIZARDDLGPROC** do provedor, enviando a mensagem WM_COMMAND com o parâmetro _wParam_ definido como WIZ_NEXT ou WIZ_PREV (dependendo de qual botão o usuário clicou). O provedor é responsável por mostrar ou ocultar seus controles e gravar seus dados no **IMAPIProp** passado para o assistente de perfil para percorrer sua sequência de páginas. O provedor deve retornar TRUE se a página seguinte ou anterior for exibida com êxito e FALSE se nem a página seguinte ou anterior puder ser exibida. O provedor precisa estar ciente de quando estiver Depurando fora de sua sequência de páginas e responder de forma adequada, ocultando seus controles e gravando seus dados no perfil. 
    
7. Se o usuário seguir as etapas de fora do intervalo de páginas do provedor, o assistente de perfil excluirá os controles ocultos do provedor da caixa de diálogo e chamará o próximo provedor ou exibirá sua próxima página se esse for o último provedor. 
    

