---
title: Modelo de objeto componente e MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cca4c70d-b73a-4834-80b5-9cb5889f63cc
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: cf687a7bfadb0981ca3440c2f81bc5de8f910924
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766312"
---
# <a name="component-object-model-and-mapi"></a>Modelo de objeto componente e MAPI

  
  
**Aplica-se a**: Outlook 
  
Documentação do SDK do Windows inclui uma discussão abrangente das regras de implementação de objetos que se ajustam para o modelo COM (Component Object). Essas regras tratam como fazer o seguinte:
  
- Objetos e interfaces de design.
    
- Implemente a interface [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx) . 
    
- Gerencie memória.
    
- Lidar com a contagem de referência.
    
- Implemente objetos de apartamento.
    
Embora todos os objetos MAPI são considerados baseado em COM, porque eles implementam as interfaces que herdam [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx), MAPI difere em determinadas situações de regras COM standard. Este desvio permite aos desenvolvedores mais flexibilidade em suas implementações. Por exemplo, uma interface MAPI, como qualquer interface COM, descreve um contrato entre o chamador e o implementador. Depois que a interface é criada e publicada, sua definição não é possível e não é alterado. MAPI não desviar dessa descrição, mas ele libera a descrição relativamente. Implementadores podem optar por não implementar os métodos específicos, o retorno de um dos seguintes valores de erro ao chamador: 
  
- MAPI_E_NO_SUPPORT
    
- MAPI_E_TOO_COMPLEX
    
- MAPI_E_BAD_CHARWIDTH
    
- MAPI_E_TYPE_NO_SUPPORT
    
Os outros desvios das regras COM standard são descritos na tabela a seguir.
  
|**Regra de programação COM**|**Variação de MAPI**|
|:-----|:-----|
|Todos os parâmetros de cadeia de caracteres nos métodos de interface devem ser Unicode.  <br/> |Interfaces MAPI são definidas para permitir que os parâmetros de cadeia de caracteres Unicode ou ANSI. Muitos métodos que têm um parâmetro de cadeia de caracteres também tem um parâmetro de **ulFlags** ; a largura de um parâmetro de cadeia de caracteres é indicada pelo valor do sinalizador MAPI_UNICODE em **ulFlags**. Algumas interfaces MAPI não oferece suporte a Unicode e retornar MAPI_E_BAD_CHARWIDTH quando o sinalizador MAPI_UNICODE é definido.  <br/> |
|Todos os métodos de interface devem ter um tipo de retorno de HRESULT.  <br/> |MAPI tem pelo menos um método que retorna um valor não-HRESULT: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).  <br/> |
|Os chamadores e implementadores devem alocar e liberar memória para os parâmetros de interface usando os alocadores de tarefa COM standard.  <br/> |Todos os métodos MAPI usam os vinculados alocadores [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)e [MAPIFreeBuffer](mapifreebuffer.md) para gerenciar memória para os parâmetros de interface. Todas as implementações de MAPI das interfaces definidos pelo OLE, como [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx), usam os alocadores de tarefa COM standard.  <br/> |
|A saída todos os parâmetros de ponteiro explicitamente devem ser definidos como NULL quando um método falha.  <br/> |Interfaces de MAPI exigem que os parâmetros de ponteiro estar definido como NULL ou permanecer inalterado quando um método de saída falhar. Todas as implementações de MAPI das interfaces definidos pelo OLE explicitamente definir parâmetros como NULL em caso de falha de saída.  <br/> |
|Implemente objetos de endereços sempre que possível.  <br/> |Interfaces MAPI não são agregáveis.  <br/> |
   
## <a name="see-also"></a>Confira também



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[Objeto MAPI e visão geral da Interface](mapi-object-and-interface-overview.md)

