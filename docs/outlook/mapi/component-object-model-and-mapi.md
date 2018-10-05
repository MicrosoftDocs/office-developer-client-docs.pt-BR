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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394115"
---
# <a name="component-object-model-and-mapi"></a>COM (Component Object Model) e MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Documentação do SDK do Windows inclui uma discussão abrangente das regras de implementação de objetos que se ajustam para o modelo COM (Component Object). Essas regras tratam como fazer o seguinte:
  
- Objetos e interfaces de design.
    
- Implemente a interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) . 
    
- Gerencie memória.
    
- Lidar com a contagem de referência.
    
- Implemente objetos de apartamento.
    
Embora todos os objetos MAPI são considerados baseado em COM, porque eles implementam as interfaces que herdam [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx), MAPI difere em determinadas situações de regras COM standard. Este desvio permite aos desenvolvedores mais flexibilidade em suas implementações. Por exemplo, uma interface MAPI, como qualquer interface COM, descreve um contrato entre o chamador e o implementador. Depois que a interface é criada e publicada, sua definição não é possível e não é alterado. MAPI não desviar dessa descrição, mas ele libera a descrição relativamente. Implementadores podem optar por não implementar os métodos específicos, o retorno de um dos seguintes valores de erro ao chamador: 
  
- MAPI_E_NO_SUPPORT
    
- MAPI_E_TOO_COMPLEX
    
- MAPI_E_BAD_CHARWIDTH
    
- MAPI_E_TYPE_NO_SUPPORT
    
Os outros desvios das regras COM standard são descritos na tabela a seguir.
  
|**Regra de programação COM**|**Variação de MAPI**|
|:-----|:-----|
|Todos os parâmetros de cadeia de caracteres nos métodos de interface devem ser Unicode.  <br/> |Interfaces MAPI são definidas para permitir que os parâmetros de cadeia de caracteres Unicode ou ANSI. Muitos métodos que têm um parâmetro de cadeia de caracteres também tem um parâmetro de **ulFlags** ; a largura de um parâmetro de cadeia de caracteres é indicada pelo valor do sinalizador MAPI_UNICODE em **ulFlags**. Algumas interfaces MAPI não oferece suporte a Unicode e retornar MAPI_E_BAD_CHARWIDTH quando o sinalizador MAPI_UNICODE é definido.  <br/> |
|Todos os métodos de interface devem ter um tipo de retorno de HRESULT.  <br/> |MAPI tem pelo menos um método que retorna um valor não-HRESULT: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).  <br/> |
|Os chamadores e implementadores devem alocar e liberar memória para os parâmetros de interface usando os alocadores de tarefa COM standard.  <br/> |Todos os métodos MAPI usam os vinculados alocadores [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)e [MAPIFreeBuffer](mapifreebuffer.md) para gerenciar memória para os parâmetros de interface. Todas as implementações de MAPI das interfaces definidos pelo OLE, como [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx), usam os alocadores de tarefa COM standard.  <br/> |
|A saída todos os parâmetros de ponteiro explicitamente devem ser definidos como NULL quando um método falha.  <br/> |Interfaces de MAPI exigem que os parâmetros de ponteiro estar definido como NULL ou permanecer inalterado quando um método de saída falhar. Todas as implementações de MAPI das interfaces definidos pelo OLE explicitamente definir parâmetros como NULL em caso de falha de saída.  <br/> |
|Implemente objetos de endereços sempre que possível.  <br/> |Interfaces MAPI não são agregáveis.  <br/> |
   
## <a name="see-also"></a>Confira também



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[Objeto MAPI e visão geral da Interface](mapi-object-and-interface-overview.md)

