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
  
Define uma função de retorno de chamada invocada pelo Assistente de Perfil para permitir que um provedor de serviços reaja a eventos de usuário quando as páginas ou folhas de propriedades do provedor estão sendo mostradas. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiwz.h  <br/> |
|Função definida implementada por:  <br/> |Provedores de serviços  <br/> |
|Função definida chamada por:  <br/> |Assistente de Perfil MAPI  <br/> |
   
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
  
> [in] Alça de janela para a caixa de diálogo Assistente de Perfil. 
    
_wMsgID_
  
> [in] A mensagem da janela a ser processada. Além das mensagens de janela regular esperadas por uma caixa de diálogo modal, as seguintes mensagens podem ser recebidas:
    
WM_CLOSE 
  
> O Assistente de Perfil foi concluído. O provedor de serviços deve fazer toda a limpeza necessária, como desalocar qualquer memória alocada dinamicamente. 
    
WM_COMMAND 
  
> Um dos controles do provedor foi  selecionado  ou o botão Próximo ou Voltar foi clicado. O valor no  _parâmetro wParam_ indica quais desses eventos de usuário ocorreram. 
    
WM_INITDIALOG 
  
> O usuário foi movido para outra página de propriedades, para a qual a caixa de diálogo deve ser inicializada. O provedor deve inicializar os controles que o Assistente de Perfil adicionou à caixa de diálogo. 
    
WIZ_QUERYNUMPAGES 
  
> O Assistente de Perfil está solicitando o número de páginas que o provedor precisa exibir. O provedor deve retornar o número de páginas em vez de VERDADEIRO ou FALSO. Por exemplo, use a seguinte instrução de retorno para indicar que três páginas devem ser exibidas:
    
   ```cpp
return (BOOL)3;

   ```

_wParam_
  
> [in] Um parâmetro de 32 bits associado a mensagens de janela. Os valores possíveis dependem da mensagem especificada no _parâmetro wMsgID._ Além dos valores esperados com as mensagens de janela regular para uma caixa de diálogo modal, os seguintes valores podem ser recebidos: 
    
WIZ_NEXT 
  
> Quando  _wMsgID_ contém WM_COMMAND, o usuário clicou no **botão** Próximo. 
    
WIZ_PREV 
  
> Quando  _wMsgID_ contém WM_COMMAND, o usuário clicou no **botão** Voltar. 
    
_lParam_
  
> [in] Um parâmetro de 32 bits associado a mensagens de janela. Os valores possíveis dependem da mensagem especificada no _parâmetro wMsgID._ 
    
## <a name="return-value"></a>Valor de retorno

O valor retornado por **uma função baseada em SERVICEWIZARDDLGPROC** depende da mensagem de janela recebida. Observe, em particular, o valor de retorno excepcional da WIZ_QUERYNUMPAGES mensagem. Os valores de retorno normais são: 
  
TRUE 
  
> O provedor de serviços processou a mensagem de janela recebida. 
    
FALSE 
  
> O provedor de serviços não processou a mensagem de janela recebida.
    
## <a name="remarks"></a>Comentários

Quando o usuário se move de uma página de propriedades para outra, o provedor é responsável por ocultar os controles da página antiga e mostrar os controles da página seguinte ou anterior. Quando o usuário  clica no botão Próximo, a função baseada **SERVICEWIZARDDLGPROC** é chamada com a mensagem WM_COMMAND e WIZ_NEXT no parâmetro _wParam._ As etapas a seguir descrevem o que ocorre entre o momento em que o usuário clica em **Next** e a hora em que as páginas de configuração do primeiro provedor são renderizadas. 
  
1. O Assistente de Perfil oculta todos os controles que estão na janela. 
    
2. O Assistente de Perfil adiciona os controles ocultos do provedor à página. 
    
3. O Assistente de Perfil **chama SERVICEWIZARDDLGPROC**, enviando a WM_INITDIALOG, para que o provedor possa inicializar os controles. 
    
4. O Assistente de Perfil **chama SERVICEWIZARDDLGPROC**, enviando a WIZ_QUERYNUMPAGES mensagem. O provedor retorna o número de páginas a serem mostradas. 
    
5. O Assistente de Perfil chama **SERVICEWIZARDDLGPROC**, enviando a mensagem WM_COMMAND com o parâmetro  _wParam_ definido como WIZ_NEXT ou WIZ_PREV. Neste ponto, o provedor retorna FALSE {error} ou revela seus controles e retorna VERDADEIRO {success}. Se o Assistente de Perfil passar ID_NEXT, a primeira página do provedor será exibida. Se ID_PREV for passada, a última página será exibida. 
    
6. O Assistente de Perfil chama a função **SERVICEWIZARDDLGPROC** do provedor, enviando WM_COMMAND mensagem com o parâmetro  _wParam_ definido como WIZ_NEXT ou WIZ_PREV (dependendo de qual botão o usuário clicou). O provedor é responsável por mostrar ou ocultar seus controles e escrever seus dados para o **IMAPIProp** passado para o Assistente de Perfil para passar por sua sequência de páginas. O provedor deverá retornar TRUE se a página seguinte ou anterior tiver sido exibida com êxito e FALSE se nem a página seguinte nem a anterior puderem ser mostradas. O provedor precisa estar ciente de quando está saindo de sua sequência de páginas e responder adequadamente ocultando seus controles e escrevendo seus dados no perfil. 
    
7. Se o usuário sair do intervalo de páginas do provedor, o Assistente de Perfil excluirá os controles ocultos do provedor da caixa de diálogo e chamará o próximo provedor ou exibirá sua próxima página se esse for o último provedor. 
    

