---
title: COM (Component Object Model) e MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cca4c70d-b73a-4834-80b5-9cb5889f63cc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a91ab8497a690fd4b99f76274d0213284253fd06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334465"
---
# <a name="component-object-model-and-mapi"></a>COM (Component Object Model) e MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A documentação do SDK do Windows inclui uma discussão abrangente das regras para implementar objetos em conformidade com o COM (Component Object Model). Essas regras abordam como fazer o seguinte:
  
- Projetar interfaces e objetos.
    
- Implemente a interface [IUnknown.](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) 
    
- Gerenciar memória.
    
- Lidar com a contagem de referências.
    
- Implemente objetos apartment-threaded.
    
Embora todos os objetos MAPI sejam considerados baseados em COM porque implementam interfaces que herdam de [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx), MAPI se desvia em algumas situações das regras COM padrão. Esse desvio permite aos desenvolvedores mais flexibilidade em suas implementações. Por exemplo, uma interface MAPI, como qualquer interface COM, descreve um contrato entre o implementador e o chamador. Depois que a interface é criada e publicada, sua definição não pode e não muda. O MAPI não se desvia dessa descrição, mas a descrição é um pouco diferente. Implementadores podem optar por não implementar métodos específicos, retornando um dos seguintes valores de erro para o chamador: 
  
- MAPI_E_NO_SUPPORT
    
- MAPI_E_TOO_COMPLEX
    
- MAPI_E_BAD_CHARWIDTH
    
- MAPI_E_TYPE_NO_SUPPORT
    
Os outros desvios das regras COM padrão são descritos na tabela a seguir.
  
|**Regra de programação COM**|**Variação MAPI**|
|:-----|:-----|
|Todos os parâmetros de cadeia de caracteres nos métodos de interface devem ser Unicode.  <br/> |As interfaces MAPI são definidas para permitir parâmetros de cadeia de caracteres Unicode ou ANSI. Muitos métodos que têm um parâmetro de cadeia de caracteres também têm um **parâmetro ulFlags;** a largura de um parâmetro de cadeia de caracteres é indicada pelo valor do MAPI_UNICODE sinalizador em **ulFlags**. Algumas interfaces MAPI não suportam Unicode e retornam MAPI_E_BAD_CHARWIDTH quando o sinalizador MAPI_UNICODE está definido.  <br/> |
|Todos os métodos de interface devem ter um tipo de retorno HRESULT.  <br/> |MAPI has at least one method that returns a non-HRESULT value: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).  <br/> |
|Os chamadores e implementadores devem alocar e liberar memória para parâmetros de interface usando os alocadores de tarefas COM padrão.  <br/> |Todos os métodos MAPI usam os alocadores vinculados [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)e [MAPIFreeBuffer](mapifreebuffer.md) para gerenciar a memória para parâmetros de interface. Todas as implementações de MAPI de interfaces definidas por OLE, como [IStream,](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)usam os alocadores de tarefas COM padrão.  <br/> |
|Todos os parâmetros de ponteiro de saída devem ser definidos explicitamente como NULL quando um método falhar.  <br/> |As interfaces MAPI exigem que os parâmetros de ponteiro de saída sejam definidos como NULL ou permaneçam inalterados quando um método falha. Todas as implementações de MAPI de interfaces definidas pelo OLE explicitamente definem parâmetros como NULL em caso de falha.  <br/> |
|Implemente objetos aggregatable sempre que possível.  <br/> |As interfaces MAPI não são aggregantes.  <br/> |
   
## <a name="see-also"></a>Confira também



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[Visão geral de objetos e interface MAPI](mapi-object-and-interface-overview.md)

