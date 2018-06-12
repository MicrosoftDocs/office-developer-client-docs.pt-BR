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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 86cd30b15402f35e8396dedf6b685050ee4fb45e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766494"
---
# <a name="dtblpage"></a>DTBLPAGE

  
  
**Aplica-se a**: Outlook 
  
Descreve uma página com guias que será usada em uma caixa de diálogo que é construída a partir de uma tabela de exibição. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
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

## <a name="members"></a>Membros

 **ulbLpszLabel**
  
> Posição na memória do rótulo caractere cadeia de caracteres para a guia página.
    
 **ulFlags**
  
> Bitmask dos sinalizadores usados para designar o formato do rótulo apontado pelo membro **ulbLpszLabelName** . O seguinte sinalizador pode ser definido: 
    
MAPI_UNICODE 
  
> O rótulo está no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, o rótulo está no formato ANSI.
    
 **ulbLpszComponent**
  
> Posição na memória de uma cadeia de caracteres que identifica a seção **[Help File Mappings]** o MAPISVC. Arquivo de configuração INF ou 0. O nome de arquivo que aparecem no MAPISVC. Seção INF pode ser usada por um usuário para acessar a ajuda estendida para a página com guias clicando no botão **Ajuda** na caixa de diálogo. Para obter mais informações sobre as entradas na MAPISVC. INF, consulte [formato de arquivo do MAPISVC. INF](file-format-of-mapisvc-inf.md).
    
 **ulContext**
  
> Um identificador exclusivo para a página com guias na cadeia de caracteres definida pelo membro **ulbLpszComponent** . O membro **ulbLpszComponent** e o membro de **ulContext** devem ser diferente de zero para o botão **Ajuda** trabalhar. Se esse identificador é zero e a cadeia de caracteres do componente for NULL, não há nenhuma ajuda associada à página. 
    
## <a name="remarks"></a>Coment�rios

Uma estrutura **DTBLPAGE** descreve uma página com guias de um controle que é usado para separar várias caixas de diálogo relacionadas. Geralmente, essas caixas de diálogo são folhas de propriedades para exibir a configuração, uma mensagem ou opções de destinatário. Ao clicar na guia, o usuário pode alternar de uma planilha para outro. 
  
O identificador de cadeia de caracteres e contexto de componente fornecem informações sobre se ajuda estendida está disponível para a página com guias. Se ajuda estendida estiver disponível, o identificador de cadeia de caracteres e o contexto do componente fornecerá informações sobre como acessá-lo. A cadeia de caracteres do componente é mapeado para o arquivo de ajuda; o identificador de contexto mapeia para o tópico de ajuda inicial. Se o identificador de contexto é zero e a cadeia de caracteres do componente for NULL, ajuda estendida não está disponível.
  
Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md). Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela exibir](display-table-implementation.md).
  
## <a name="see-also"></a>Confira também



[DTCTL](dtctl.md)


[Estruturas MAPI](mapi-structures.md)

