---
title: OLFI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 44bfaadf-36f9-bd8e-6158-646533f6849e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 027905721b5730b4c3d78f496022b88a8e6b84d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279750"
---
# <a name="olfi"></a>OLFI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fila de estruturas de ID de longo prazo usadas pelo provedor de repositório de arquivos de pastas particulares (PST) para atribuir uma ID de entrada para uma nova mensagem ou pasta no modo offline.
  
## <a name="quick-info"></a>Informações rápidas

```cpp
typedef struct { 
    ULONG    ulVersion; 
    MAPIUID  muidReserved; 
    ULONG    ulReserved; 
    DWORD    dwAlloc; 
    DWORD    dwNextAlloc; 
    LTID     ltidAlloc; 
    LTID     ltidNextAlloc; 
} OLFI, *POLFI;
```

## <a name="members"></a>Membros

 _ulVersion_
  
- Número de versão da estrutura. 
    
 _muidReserved_
  
- Este membro é reservado para uso interno do Outlook e não tem suporte.
    
 _ulReserved_
  
- Este membro é reservado para uso interno do Outlook e não tem suporte.
    
 _dwAlloc_
  
- O número de entradas disponíveis para alocação. Essas entradas compartilham o mesmo identificador global exclusivo (GUID).
    
 _dwNextAlloc_
  
- O número de entradas disponíveis ao lado da alocação. Essas entradas compartilham o mesmo GUID.
    
 _ltidAlloc_
  
- A estrutura de ID de longo prazo, **[ltid](ltid.md)**, identificando a entrada atualmente disponível para alocação. A estrutura de ID de longo prazo contém um GUID e um índice que identifica um objeto no repositório. Juntos, o GUID e o índice podem formar uma ID de entrada exclusiva para um objeto. 
    
 _ltidNextAlloc_
  
- Estrutura de ID de longo prazo identificando a próxima entrada disponível.
    
## <a name="remarks"></a>Comentários

Uma ID de entrada é um identificador de entrada MAPI de 4 bytes para uma pasta ou uma mensagem. Para obter mais informações, [](https://msdn.microsoft.com/library/ms836424)consulte EntryID.
  
Quando um provedor de repositório PST atribui uma ID de entrada a um novo objeto, ele primeiro precisa de um GUID que identifique o servidor e um índice que identifique o objeto no repositório. Mesmo que o GUID não seja exclusivo em todas as IDs de entrada, o GUID e o índice combinados fornecem uma entrada exclusiva. Este par de GUIDs e de índice é rastreado por uma estrutura de ID de longo prazo, **ltid**, que é parte da estrutura **OLFI** . 
  
O provedor de repositório PST não mantém fisicamente no **OLFI** uma estrutura **ltid** para cada par GUID-index. Ele mantém uma estrutura **ltid** , *ltidAlloc* , para o primeiro par de índice GUID disponível no momento; uma contagem, *dwAlloc* , do número de entradas disponíveis que compartilham esse mesmo GUID; e uma segunda estrutura **ltid** , *ltidNextAlloc* , para o próximo par de índice GUID disponível que tem um GUID diferente. O provedor de repositório PST usa a estrutura **OLFI** para controlar os GUIDs e índices que ele colocou. Em um nível virtual, o provedor mantém uma reserva de várias estruturas do **ltid** que estão prontas para serem alocadas.  *dwAlloc* mantém uma contagem das estruturas **ltid** disponíveis. 
  
As solicitações de IDs de entrada são incluídas em blocos. Quando houver uma solicitação para um bloco, o provedor do repositório PST verificará se há reserva suficiente à mão comparando o tamanho solicitado com *dwAlloc* . Se houver uma reserva suficiente, ela retornará o GUID e o índice em *ltidAlloc* para alocação. Em seguida, ele diminui *dwAlloc* pelo tamanho solicitado e incrementa o índice em *ltidAlloc* pelo tamanho solicitado. Isso prepara o provedor do repositório PST para alocar *ltidAlloc* na próxima solicitação para outro bloco de IDs de entrada. Observe que o GUID permanece o mesmo para a próxima solicitação. 
  
Se o tamanho de uma solicitação for maior do que *dwAlloc* , o provedor do repositório PST tentará usar o próximo na reserva, conforme especificado por *dwNextAlloc* e *ltidNextAlloc* . Ele copia *dwNextAlloc* e *LtidNextAlloc* para o *dwAlloc* e o *ltidAlloc* respectivamente e define *dwNextAlloc* e *ltidNextAlloc* como nulo. 
  
Um provedor que encapsula o provedor de repositório PST deve verificar periodicamente o *ltidNextAlloc* para ver se ele é nulo. Se for, o provedor deverá preenchê-lo com um novo GUID e redefinir *dwNextAlloc* para que mais IDs de entrada possam ser alocadas. 
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[LTID](ltid.md)

