---
title: DTBLBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLBUTTON
api_type:
- COM
ms.assetid: 6058c78b-05d4-45a3-988c-1fbf8322125e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e0797364eb4ec24793f64bad2f4d838507c236e4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571063"
---
# <a name="dtblbutton"></a>DTBLBUTTON

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém informações sobre um controle de botão para uma caixa de diálogo construída a partir de uma tabela de exibição.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Macro relacionada:  <br/> |[SizedDtblButton](sizeddtblbutton.md) <br/> |
   
```cpp
typedef struct _DTBLBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRControl;
} DTBLBUTTON, FAR *LPDTBLBUTTON;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> Posição na memória da sequência de caracteres que é exibida no botão.
    
 **ulFlags**
  
> Bitmask dos sinalizadores usados para designar o formato do rótulo apontado pelo membro **ulbLpszLabel** . O seguinte sinalizador pode ser definido: 
    
MAPI_UNICODE 
  
> O rótulo está no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, o rótulo está no formato ANSI.
    
 **ulPRControl**
  
> Marca de propriedade para uma propriedade do tipo PT_OBJECT que implementa a interface [IMAPIControl](imapicontroliunknown.md) . Quando o botão é clicado, MAPI chama o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para a implementação de [IMAPIProp](imapipropiunknown.md) de exibição da tabela recuperar essa propriedade. 
    
## <a name="remarks"></a>Comentários

Uma estrutura **DTBLBUTTON** descreve um botão de um controle que, quando clicado, permite que um usuário iniciar uma operação. Normalmente, clicando em um botão faz com que uma caixa de diálogo de janela restrita a ser exibido ou uma tarefa programática a ser chamado. Provedores de serviço podem implementar nada através de um controle de botão. Se o botão deve para executar uma tarefa com base nos valores dos outros controles, esses controles devem ter configurado o sinalizador DT_SET_IMMEDIATE. 
  
O membro **ulbLpszLabel** é a posição na memória da sequência de caracteres que é exibida no botão. Provedores de serviços podem adicionar um caractere (&amp;) para indicar um acelerador do Windows em que o rótulo do botão. Pressionar uma tecla aceleradora tem o mesmo efeito que clicar no botão. 
  
O membro **ulPRControl** descreve uma propriedade de um objeto que, quando aberto com o método **IMAPIProp::OpenProperty** , retorna um ponteiro para um objeto control. A implementação de um objeto de controle que oferece suporte à interface **IMAPIControl** é uma maneira de estender o conjunto de recursos do MAPI e definir a operação ou tarefa que ocorre quando o botão é clicado. **IMAPIControl** fornece dois métodos para manipulá-lo botões: [GetState](imapicontrol-getstate.md) para desabilitar ou habilitar botões e [Ativar](imapicontrol-activate.md) lidar com cliques de botão. 
  
Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md). Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela exibir](display-table-implementation.md).
  
## <a name="see-also"></a>Confira também



[DTCTL](dtctl.md)


[Estruturas MAPI](mapi-structures.md)

