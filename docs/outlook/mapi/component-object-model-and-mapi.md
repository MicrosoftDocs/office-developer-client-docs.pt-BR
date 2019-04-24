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
  
A documentação do SDK do Windows inclui uma discussão abrangente das regras para implementar objetos que estão de acordo com o modelo de objeto componente (COM). Essas regras abordam como fazer o seguinte:
  
- Criar interfaces e objetos.
    
- Implementar a interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) . 
    
- Gerenciar memória.
    
- Gerenciar contagem de referência.
    
- Implementar objetos Apartment-Threaded.
    
Embora todos os objetos MAPI sejam considerados com base em COM, pois implementam interfaces que herdam de [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx), o MAPI desvia em algumas situações das regras com padrão. Esse desvio permite que os desenvolvedores tenham mais flexibilidade em suas implementações. Por exemplo, uma interface MAPI, como qualquer interface COM, descreve um contrato entre o implementador e o chamador. Depois que a interface é criada e publicada, sua definição não pode e não é alterada. O MAPI não se desvia dessa descrição, mas libera, de certa forma, a descrição. Os implementadores podem optar por não implementar métodos específicos, retornando um dos seguintes valores de erro ao chamador: 
  
- MAPI_E_NO_SUPPORT
    
- MAPI_E_TOO_COMPLEX
    
- MAPI_E_BAD_CHARWIDTH
    
- MAPI_E_TYPE_NO_SUPPORT
    
Os outros desvios das regras COM padrão são descritos na tabela a seguir.
  
|**Regra de programação COM**|**Variação de MAPI**|
|:-----|:-----|
|Todos os parâmetros de cadeia de caracteres nos métodos de interface devem ser Unicode.  <br/> |As interfaces MAPI são definidas para permitir parâmetros de cadeia de caracteres Unicode ou ANSI. Muitos métodos que possuem um parâmetro de cadeia de caracteres também têm um parâmetro **parâmetroulflags** ; a largura de um parâmetro de cadeia de caracteres é indicada pelo valor do sinalizador MAPI_UNICODE em **parâmetroulflags**. Algumas interfaces MAPI não dão suporte a Unicode e retornam MAPI_E_BAD_CHARWIDTH quando o sinalizador MAPI_UNICODE está definido.  <br/> |
|Todos os métodos de interface devem ter um tipo de retorno HRESULT.  <br/> |O MAPI tem pelo menos um método que retorna um valor não HRESULT: [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md).  <br/> |
|Os chamadores e implementadores devem alocar e liberar memória para os parâmetros de interface usando os alocadores de tarefa COM padrão.  <br/> |Todos os métodos MAPI usam os alocadores vinculados [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)e [MAPIFreeBuffer](mapifreebuffer.md) para gerenciar memória para parâmetros de interface. Todas as implementações MAPI de interfaces definidas por OLE, como [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx), usam os alocadores de tarefa com padrão.  <br/> |
|Todos os parâmetros de ponteiro devem ser definidos explicitamente como NULL quando um método falha.  <br/> |As interfaces MAPI exigem que os parâmetros de ponteiro de saída sejam definidos como nulos ou permaneçam inalterados quando um método falha. Todas as implementações de MAPI de interfaces definidas por OLE explicitamente definem parâmetros como NULL em Failure.  <br/> |
|Implemente objetos agregáveis sempre que possível.  <br/> |As interfaces MAPI não podem ser agregadas.  <br/> |
   
## <a name="see-also"></a>Confira também



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[Visão geral de interface e objeto MAPI](mapi-object-and-interface-overview.md)

