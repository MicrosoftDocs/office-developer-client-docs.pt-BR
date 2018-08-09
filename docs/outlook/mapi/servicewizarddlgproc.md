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
ms.openlocfilehash: 649046aa48f293caa5bd71cc670481b5c205459a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770383"
---
# <a name="servicewizarddlgproc"></a>SERVICEWIZARDDLGPROC
 
**Aplica-se a**: Outlook 
  
Define uma função de retorno de chamada invocada pelo Assistente de perfil para permitir que um provedor de serviços reajam a eventos quando estão sendo mostradas folhas de propriedades ou a páginas do provedor do usuário. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiwz.h  <br/> |
|Função definido implementada por:  <br/> |Provedores de serviços  <br/> |
|Função definido chamada pelo:  <br/> |Assistente de perfil MAPI  <br/> |
   
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
  
> [in] Identificador da janela para a caixa de diálogo Assistente de perfil. 
    
_wMsgID_
  
> [in] A mensagem da janela a ser processado. Além das mensagens de janela regular esperadas por uma caixa de diálogo de janela restrita, as seguintes mensagens podem ser recebidas:
    
WM_CLOSE 
  
> O Assistente de perfil for concluído. O provedor de serviços deve fazer todas as limpeza necessária como desalocar qualquer dinamicamente memória alocada. 
    
WM_COMMAND 
  
> Um dos controles do provedor foi selecionado ou o botão **Avançar** ou **Voltar** foi clicado. O valor no parâmetro _wParam_ indica qual desses eventos de usuário tenha ocorrido. 
    
WM_INITDIALOG 
  
> O usuário foi movido para outra página de propriedade, para o qual a caixa de diálogo deve ser inicializada. O provedor deve inicializar os controles que o Assistente de perfil adicionada à caixa de diálogo. 
    
WIZ_QUERYNUMPAGES 
  
> O Assistente de perfil está solicitando o número de páginas que o provedor precisa ser exibido. O provedor deve retornar o número de páginas em vez de TRUE ou FALSE. Por exemplo, use a seguinte instrução de retorno para indicar que três páginas devem para ser exibida:
    
   ```cpp
return (BOOL)3;

   ```

_wParam_
  
> [in] Um parâmetro de 32 bits associado a mensagens de janela. Os valores possíveis dependem a mensagem especificada no parâmetro _wMsgID_ . Além dos valores esperados com as mensagens de janela normal para uma caixa de diálogo modal, os seguintes valores podem ser recebidos: 
    
WIZ_NEXT 
  
> Quando _wMsgID_ contém WM_COMMAND, o usuário clicou no botão **Avançar** . 
    
WIZ_PREV 
  
> Quando _wMsgID_ contém WM_COMMAND, o usuário clicou no botão **Voltar** . 
    
_lParam_
  
> [in] Um parâmetro de 32 bits associado a mensagens de janela. Os valores possíveis dependem a mensagem especificada no parâmetro _wMsgID_ . 
    
## <a name="return-value"></a>Valor retornado

O valor retornado por uma função **SERVICEWIZARDDLGPROC** com base é dependente a janela mensagem recebida. Em particular, observe que o excepcionais para a mensagem WIZ_QUERYNUMPAGES o valor de retorno. Os valores de retorno normais são: 
  
VERDADEIRO 
  
> O provedor de serviços tiver processado a mensagem recebida de janela. 
    
FALSO 
  
> O provedor de serviços não processado a mensagem recebida de janela.
    
## <a name="remarks"></a>Comentários

Quando o usuário move na página de propriedades de um para outro, o provedor é responsável por ocultar os controles da página antiga e mostrando os controles da página anterior ou seguinte. Quando o usuário clica no botão **Avançar** , a função **SERVICEWIZARDDLGPROC** com base é chamada com a mensagem WM_COMMAND e WIZ_NEXT no parâmetro _wParam_ . As seguintes etapas descrevem o que ocorre entre o momento em que o usuário clica em **Avançar** e o tempo de que páginas de configuração do provedor a primeira são processadas. 
  
1. O Assistente de perfil oculta todos os controles que estão na janela. 
    
2. O Assistente de perfil adiciona controles de ocultos do provedor à página. 
    
3. O Assistente de perfil chama **SERVICEWIZARDDLGPROC**, enviando a mensagem WM_INITDIALOG, para que o provedor pode inicializar os controles. 
    
4. O Assistente de perfil chama **SERVICEWIZARDDLGPROC**, enviando a mensagem WIZ_QUERYNUMPAGES. O provedor retorna o número de páginas que devem ser mostrados. 
    
5. O Assistente de perfil chama **SERVICEWIZARDDLGPROC**, enviando a mensagem WM_COMMAND com o parâmetro _wParam_ definido como WIZ_NEXT ou WIZ_PREV. Neste ponto, o provedor tanto retorna FALSE {erro} ou revela seus controles e retorna verdadeiro {sucesso}. Se o Assistente de perfil passa no ID_NEXT, a página do provedor primeira é exibida. Se ID_PREV for passado, a última página é exibida. 
    
6. O Assistente de perfil chama a função **SERVICEWIZARDDLGPROC** do provedor, enviando a mensagem WM_COMMAND com o parâmetro _wParam_ definido como WIZ_NEXT ou WIZ_PREV (dependendo de qual botão o usuário clicou). O provedor é responsável por mostrar ou ocultar seus controles e gravando seus dados para o **IMAPIProp** passados para o Assistente de perfil para percorrer sua sequência de páginas. O provedor deve retornar TRUE se a página anterior ou seguinte foi exibida com êxito, e FALSE se nem a página próxima nem anterior puderam ser mostrada. O provedor precisa estar ciente quando ele está se preparando fora de sua sequência de páginas e responder apropriadamente ocultando seus controles e gravando seus dados para o perfil. 
    
7. Se o usuário etapas fora do intervalo do provedor de páginas, o Assistente de perfil e exclui a controles de ocultos do provedor de caixa de diálogo chama o provedor próximo ou exibe sua próxima página se que foi o último provedor. 
    

