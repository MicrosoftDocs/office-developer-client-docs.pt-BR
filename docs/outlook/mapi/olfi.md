---
title: OLFI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 44bfaadf-36f9-bd8e-6158-646533f6849e
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 027905721b5730b4c3d78f496022b88a8e6b84d6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397020"
---
# <a name="olfi"></a>OLFI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fila de longo prazo estruturas de ID usado pelo provedor de repositório de pastas particulares (. PST) do arquivo para atribuir uma ID de entrada para uma nova mensagem ou a pasta no modo offline.
  
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

## <a name="members"></a>Members

 _ulVersion_
  
- Número de versão para a estrutura. 
    
 _muidReserved_
  
- Este membro é reservado para uso interno do Outlook e não é suportado.
    
 _ulReserved_
  
- Este membro é reservado para uso interno do Outlook e não é suportado.
    
 _dwAlloc_
  
- O número de entradas que estão disponíveis para alocação. Essas entradas compartilham o mesmo identificador globalmente exclusivo (GUID).
    
 _dwNextAlloc_
  
- O número de entradas que estão disponíveis em seguida para alocação. Essas entradas compartilham o mesmo GUID.
    
 _ltidAlloc_
  
- A longo prazo ID estrutura, **[LTID](ltid.md)**, que identifica a entrada atualmente disponível para alocação. A estrutura de ID de longo prazo contém um GUID e um índice identificando um objeto no repositório. Juntos, o GUID e o índice podem formar uma ID exclusiva de entrada para um objeto. 
    
 _ltidNextAlloc_
  
- Estrutura de ID longo prazo identificando a próxima entrada disponível.
    
## <a name="remarks"></a>Comentários

Uma identificação de entrada é um identificador de entrada MAPI de 4 bytes para uma pasta ou uma mensagem. Para obter mais informações, consulte [ENTRYID](https://msdn.microsoft.com/library/ms836424).
  
Quando um provedor de armazenamento de PST atribui uma identificação de entrada para um novo objeto, ele primeiro precisa um GUID que identifica o servidor e um índice que identifica o objeto no repositório. Embora não seja o GUID exclusivo entre todas as identificações de entrada, o GUID e o índice combinados fornecem uma entrada única. Esse par GUID e o índice é controlado por uma longo prazo estrutura de ID, **LTID**, que é parte da estrutura de **OLFI** . 
  
O provedor de repositórios de PST não fisicamente lembre **OLFI** uma estrutura **LTID** para cada par de índice de GUID. Ele mantém uma estrutura **LTID** , *ltidAlloc* , para o par de índice do GUID disponível atualmente primeiro; uma contagem, *dwAlloc* , do número de entradas disponíveis que compartilham esse mesmo GUID; e uma estrutura **LTID** segunda, *ltidNextAlloc* , para o próximo par de índice do GUID disponível que tenha um GUID diferente. O PST armazenar provedor usa a estrutura **OLFI** para controlar os GUIDs e índices que ele tem atribuídas. Em um nível virtual, o provedor mantém uma reserva de um número de estruturas **LTID** que estão prontos para ser alocado.  *dwAlloc* mantém uma contagem das estruturas **LTID** disponíveis. 
  
Solicitações de identificações de entrada vêm em blocos. Quando há uma solicitação para um bloco, o provedor de repositórios de PST verifica se há reserva suficiente disponível, comparando o tamanho solicitado com *dwAlloc* . Se houver reserva suficiente, ele retorna o GUID e o índice *ltidAlloc* para alocação. Ela diminui *dwAlloc* pelo tamanho solicitado e incrementa o índice em *ltidAlloc* pelo tamanho solicitado. Prepara o provedor de repositórios de PST alocar *ltidAlloc* na próxima solicitação para outro bloco de identificações de entrada. Observe que o GUID permanece o mesmo para a próxima solicitação. 
  
Se o tamanho de uma solicitação for maior que *dwAlloc* , o provedor de repositórios de PST tenta usar o que ele tem Avançar na reserva, conforme especificado por *dwNextAlloc* e *ltidNextAlloc* . Ela copia *dwNextAlloc* e *ltidNextAlloc* *dwAlloc* e *ltidAlloc* , respectivamente e define *dwNextAlloc* e *ltidNextAlloc* como NULL. 
  
Um provedor que envolve o provedor de repositório PST deve verificar periodicamente *ltidNextAlloc* para ver se ele é NULL. Se estiver, o provedor deve preenchê-lo com um novo GUID e redefinir *dwNextAlloc* , de modo que as IDs de entradas mais podem ser alocada. 
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[LTID](ltid.md)

