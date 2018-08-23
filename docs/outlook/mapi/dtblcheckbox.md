---
title: DTBLCHECKBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLCHECKBOX
api_type:
- COM
ms.assetid: 0dd12990-5431-4768-9d64-27d4ef6b7b20
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fa7f6ac116bf5255d2598465085bab2695ae2c25
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564511"
---
# <a name="dtblcheckbox"></a>DTBLCHECKBOX

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém informações sobre uma caixa de seleção que será usada em uma caixa de diálogo construída a partir de uma tabela de exibição. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Macro relacionada:  <br/> |[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |
   
```cpp
typedef struct _DTBLCHECKBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRPropertyName;
} DTBLCHECKBOX, FAR *LPDTBLCHECKBOX;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> Posição na memória da sequência de caracteres que é exibida com a caixa de seleção. 
    
 **ulFlags**
  
> Bitmask dos sinalizadores usado para designar o formato do rótulo da caixa de seleção. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> O rótulo está no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, o rótulo está no formato ANSI.
    
 **ulPRPropertyName**
  
> Marca de propriedade para uma propriedade do tipo PT_BOOLEAN. O valor dessa propriedade é afetado pelo estado da caixa de seleção.
    
## <a name="remarks"></a>Comentários

Uma estrutura **DTBLCHECKBOX** descreve uma caixa de seleção de um controle que reflete a um dos dois estados: habilitado (uma caixa checked) ou não (uma caixa vazia). 
  
O membro **ulPRPropertyName** descreve uma propriedade booleana cujo valor é manipulado, alterando o estado da caixa de seleção. Quando a caixa de seleção é exibida pela primeira vez, MAPI chama o método de **GetProps** da implementação **IMAPIProp** associado com a tabela de exibição para recuperar um conjunto de propriedades padrão. Se uma das propriedades é mapeado para a marca de propriedade na estrutura de **DTBLCHECKBOX** , o valor para essa propriedade é exibido como o valor inicial da caixa de seleção. 
  
Controles de caixa de seleção podem ser pode ser modificados. Isso permite que um usuário alterar seus estados. Caixas de seleção modificáveis definir o sinalizador DT_EDITABLE no membro **ulCtlFlags** sua estrutura [DTCTL](dtctl.md) e sua propriedade **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)). Quando uma caixa de seleção é alterada seu estado, chamadas de MAPI [IMAPIProp::SetProps](imapiprop-setprops.md) para definir a propriedade identificada no membro de marca de propriedade da estrutura de **DTBLCHECKBOX** para o novo estado. 
  
Por exemplo, um provedor de catálogo de endereços pode incluir um controle de caixa de seleção modificável em sua caixa de diálogo de configuração para ajustar a configuração da propriedade de **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) de um destinatário. Quando o usuário seleciona a caixa de seleção, MAPI define essa propriedade como TRUE. Quando a caixa de seleção estiver desmarcada, a propriedade é definida como FALSE.
  
Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md). Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela exibir](display-table-implementation.md). Para obter informações sobre os tipos de propriedade, consulte [Visão geral do tipo de propriedade de MAPI](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Confira também



[DTCTL](dtctl.md)
  
[Propriedade canônica PidTagControlType](pidtagcontroltype-canonical-property.md)


[Estruturas MAPI](mapi-structures.md)

