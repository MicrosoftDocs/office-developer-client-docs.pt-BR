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
ms.openlocfilehash: a8fa683fecd59ec813fee0c15d5b4f08084c645d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412783"
---
# <a name="dtblbutton"></a>DTBLBUTTON

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém informações sobre um controle de botão para uma caixa de diálogo criada a partir de uma tabela de exibição.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
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
  
> Posição na memória da cadeia de caracteres que é exibida no botão.
    
 **ulFlags**
  
> Bitmask dos sinalizadores usados para designar o formato do rótulo apontado pelo membro **ulbLpszLabel** . O seguinte sinalizador pode ser definido: 
    
MAPI_UNICODE 
  
> O rótulo está no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, o rótulo estará no formato ANSI.
    
 **ulPRControl**
  
> Marca de propriedade de uma propriedade do tipo PT_OBJECT que implementa a interface [IMAPIControl](imapicontroliunknown.md) . Quando o botão é clicado, MAPI chama o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) da implementação [IMAPIProp](imapipropiunknown.md) da tabela de exibição para recuperar essa propriedade. 
    
## <a name="remarks"></a>Comentários

Uma estrutura **DTBLBUTTON** descreve um botão com um controle que, quando clicado, permite que um usuário inicie uma operação. Normalmente, clicar em um botão faz com que uma caixa de diálogo modal seja exibida ou uma tarefa programática seja invocada. Os provedores de serviços podem implementar qualquer coisa por meio de um controle de botão. Se o botão deve executar uma tarefa com base nos valores de outros controles, esses controles devem ter definido o sinalizador DT_SET_IMMEDIATE. 
  
O membro **ulbLpszLabel** é a posição na memória da cadeia de caracteres que é exibida no botão. Os provedores de serviços podem adicionar um caractere&amp;de e comercial () para indicar um aceleraDor do Windows no rótulo do botão. O pressionamento de uma tecla de aceleração tem o mesmo efeito que clicar no botão. 
  
O membro **ulPRControl** descreve uma propriedade de objeto que, quando aberta com o método **IMAPIProp:: OpenProperty** , retorna um ponteiro para um objeto Control. A implementação de um objeto Control que oferece suporte à interface **IMAPIControl** é uma maneira de estender o conjunto de recursos MAPI e definir a operação ou tarefa que ocorre quando o botão é clicado. O **IMAPIControl** fornece dois métodos para manipular botões: [GetState](imapicontrol-getstate.md) para desabilitar ou Habilitar botões e [Ativar](imapicontrol-activate.md) para lidar com cliques de botão. 
  
Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md). Para obter informações sobre como implementar uma tabela de exibição, consulte [implementando uma tabela de exibição](display-table-implementation.md).
  
## <a name="see-also"></a>Confira também



[DTCTL](dtctl.md)


[Estruturas MAPI](mapi-structures.md)

