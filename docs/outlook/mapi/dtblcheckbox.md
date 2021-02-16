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
ms.openlocfilehash: ed0bbe986f374648e2ee85f3a0d2dfe7bc392e0f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436829"
---
# <a name="dtblcheckbox"></a>DTBLCHECKBOX

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém informações sobre uma caixa de seleção que será usada em uma caixa de diálogo criada a partir de uma tabela de exibição. 
  
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
  
> Posição na memória da cadeia de caracteres exibida com a caixa de seleção. 
    
 **ulFlags**
  
> Bitmask de sinalizadores usados para designar o formato do rótulo da caixa de seleção. O sinalizador a seguir pode ser definido:
    
MAPI_UNICODE 
  
> O rótulo está no formato Unicode. Se o MAPI_UNICODE sinalizador não estiver definido, o rótulo está no formato ANSI.
    
 **ulPRPropertyName**
  
> Marca de propriedade de uma propriedade do tipo PT_BOOLEAN. O valor dessa propriedade é afetado pelo estado da caixa de seleção.
    
## <a name="remarks"></a>Comentários

Uma **estrutura DTBLCHECKBOX** descreve uma caixa de seleção de um controle que reflete um dos dois estados: habilitado (uma caixa de seleção) ou desabilitado (uma caixa vazia). 
  
O **membro ulPRPropertyName** descreve uma propriedade Boolean cujo valor é manipulado alterando o estado da caixa de seleção. Quando a caixa de seleção é exibida pela primeira vez, o MAPI chama o método **GetProps** da implementação **IMAPIProp** que está associada à tabela de exibição para recuperar um conjunto de propriedades padrão. Se uma das propriedades for mapeada para a marca de propriedade na estrutura **DTBLCHECKBOX,** o valor dessa propriedade será exibido como o valor inicial da caixa de seleção. 
  
Os controles de caixa de seleção podem ser modificados. Isso permite que um usuário altere seus estados. As caixas de seleção modificáveis configuram o sinalizador DT_EDITABLE no **membro ulCtlFlags** de sua estrutura [DTCTL](dtctl.md) e em sua propriedade **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)). Quando uma caixa de seleção altera seu estado, MAPI chama [IMAPIProp::SetProps](imapiprop-setprops.md) para definir a propriedade identificada no membro da marca de propriedade da estrutura **DTBLCHECKBOX** para o novo estado. 
  
Por exemplo, um provedor de livro de endereços pode incluir um controle de caixa de seleção modificável em sua caixa de diálogo de configuração para ajustar a configuração da propriedade **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) de um destinatário. Quando o usuário marca a caixa de seleção, MAPI define essa propriedade como TRUE. Quando a caixa de seleção é desa eleita, a propriedade é definida como FALSE.
  
Para uma visão geral das tabelas de exibição, consulte [Tabelas de Exibição.](display-tables.md) Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela de exibição.](display-table-implementation.md) Para obter informações sobre tipos de propriedade, consulte [Visão geral do tipo de propriedade MAPI.](mapi-property-type-overview.md)
  
## <a name="see-also"></a>Confira também



[DTCTL](dtctl.md)
  
[Propriedade canônica PidTagControlType](pidtagcontroltype-canonical-property.md)


[Estruturas MAPI](mapi-structures.md)

