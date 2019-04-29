---
title: DTBLPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLPAGE
api_type:
- COM
ms.assetid: f899f434-a5d7-4b4f-98f9-c14c9f21b24b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6f3d98a3133d79f78f4eb676d49ec85ef5a359f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423997"
---
# <a name="dtblpage"></a>DTBLPAGE

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma página com guias que será usada em uma caixa de diálogo criada a partir de uma tabela de exibição. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Macro relacionada:  <br/> |[SizedDtblPage](sizeddtblpage.md) <br/> |
   
```cpp
typedef struct _DTBLPAGE
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulbLpszComponent;
  ULONG ulContext;
} DTBLPAGE, FAR *LPDTBLPAGE;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> Posição na memória do rótulo de cadeia de caracteres para a guia de página.
    
 **ulFlags**
  
> Bitmask dos sinalizadores usados para designar o formato do rótulo apontado pelo membro **ulbLpszLabelName** . O seguinte sinalizador pode ser definido: 
    
MAPI_UNICODE 
  
> O rótulo está no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, o rótulo estará no formato ANSI.
    
 **ulbLpszComponent**
  
> Posição na memória de uma cadeia de caracteres que identifica a seção **[help file Mappings]** no MAPISVC. Arquivo de configuração INF ou 0. O nome do arquivo que aparece no MAPISVC. A seção INF pode ser usada por um usuário para acessar a ajuda estendida para a página com guias clicando no botão **ajuda** na caixa de diálogo. Para obter mais informações sobre as entradas em MAPISVC. INF, consulte [formato de arquivo de MAPISVC. INF](file-format-of-mapisvc-inf.md).
    
 **ulContext**
  
> Um identificador exclusivo para a página com guias na cadeia de caracteres definida pelo membro **ulbLpszComponent** . O membro **ulbLpszComponent** e o membro **ulContext** devem ser diferentes de zero para que o botão **ajuda** funcione. Se esse identificador for zero e a cadeia de caracteres do componente for nula, não haverá ajuda associada à página. 
    
## <a name="remarks"></a>Comentários

Uma estrutura **DTBLPAGE** descreve uma página com guias um controle que é usado para separar várias caixas de diálogo relacionadas. Normalmente, essas caixas de diálogo são folhas de propriedades para exibir opções de configuração, mensagem ou destinatário. Ao clicar na guia, o usuário pode alternar de uma planilha para outra. 
  
A cadeia de caracteres do componente e o identificador de contexto fornecem informações sobre se a ajuda estendida está disponível para a página com guias. Se a ajuda estendida estiver disponível, a cadeia de caracteres do componente e o identificador de contexto fornecerão informações sobre como acessá-lo. A cadeia de caracteres do componente mapeia para o arquivo de ajuda; o identificador de contexto é mapeado para o tópico de ajuda inicial. Se o identificador de contexto for zero e a cadeia de caracteres do componente for nula, a ajuda estendida não estará disponível.
  
Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md). Para obter informações sobre como implementar uma tabela de exibição, consulte [implementando uma tabela de exibição](display-table-implementation.md).
  
## <a name="see-also"></a>Confira também



[DTCTL](dtctl.md)


[Estruturas MAPI](mapi-structures.md)

