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
  
Fila de estruturas de ID de longo prazo usadas pelo provedor de armazenamento do arquivo de Pastas Particulares (PST) para atribuir uma ID de entrada para uma nova mensagem ou pasta no modo offline.
  
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
  
- Número da versão da estrutura. 
    
 _muidReserved_
  
- Este membro é reservado para uso interno do Outlook e não tem suporte.
    
 _ulReserved_
  
- Este membro é reservado para uso interno do Outlook e não tem suporte.
    
 _dwAlloc_
  
- O número de entradas disponíveis para alocação. Essas entradas compartilham o mesmo identificador global exclusivo (GUID).
    
 _dwNextAlloc_
  
- O número de entradas disponíveis em seguida para alocação. Essas entradas compartilham o mesmo GUID.
    
 _ltidAlloc_
  
- A estrutura de ID de longo prazo, **[LTID](ltid.md)**, identificando a entrada atualmente disponível para alocação. A estrutura de ID de longo prazo contém um GUID e um índice que identifica um objeto no armazenamento. Juntos, o GUID e o índice podem formar uma ID de entrada exclusiva para um objeto. 
    
 _ltidNextAlloc_
  
- Estrutura de ID de longo prazo identificando a próxima entrada disponível.
    
## <a name="remarks"></a>Comentários

Uma identificação de entrada é um identificador de entrada MAPI de 4 byte para uma pasta ou uma mensagem. Para obter mais informações, consulte [ENTRYID](https://msdn.microsoft.com/library/ms836424).
  
Quando um provedor de armazenamento PST atribui uma identificação de entrada a um novo objeto, ele primeiro precisa de um GUID que identifica o servidor e um índice que identifica o objeto no armazenamento. Embora o GUID não seja exclusivo em todas as IDs de entrada, o GUID e o índice combinados fornecem uma entrada exclusiva. Esse GUID e par de índices são acompanhados por uma estrutura de ID de longo prazo, **LTID**, que faz parte da **estrutura OLFI.** 
  
O provedor de armazenamento PST não mantém fisicamente em **OLFI** uma estrutura **LTID** para cada par guid-índice. Ele mantém uma **estrutura LTID,**  *ltidAlloc*  , para o primeiro par de guid-índice disponível no momento; uma contagem,  *dwAlloc*  , do número de entradas disponíveis que compartilham esse mesmo GUID; e uma segunda **estrutura LTID,**  *ltidNextAlloc*  , para o próximo par de índice GUID disponível que tem um GUID diferente. O provedor de armazenamento PST usa a estrutura **OLFI** para controlar os GUIDs e índices que ele distribuiu. Em um nível virtual, o provedor mantém uma reserva de várias estruturas **LTID** que estão prontas para serem alocadas.  *dwAlloc*  mantém uma contagem das estruturas **LTID** disponíveis. 
  
As solicitações de IDs de entrada vêm em blocos. Quando há uma solicitação de bloqueio, o provedor de armazenamento PST verifica se há reserva suficiente disponível comparando o tamanho solicitado com  *dwAlloc*  . Se houver reserva suficiente, ele retornará o GUID e o índice em  *ltidAlloc*  para alocação. Em seguida, diminui  *dwAlloc*  pelo tamanho solicitado e incrementa o índice em  *ltidAlloc*  pelo tamanho solicitado. Isso prepara o provedor de armazenamento PST para alocar  *ltidAlloc*  na próxima solicitação para outro bloco de IDs de entrada. Observe que o GUID permanece o mesmo para a próxima solicitação. 
  
Se o tamanho de uma solicitação for maior que  *dwAlloc*  , o provedor de armazenamento PST tenta usar o que tem em seguida na reserva, conforme especificado por  *dwNextAlloc*  e  *ltidNextAlloc*  . Ela copia  *dwNextAlloc*  e  *ltidNextAlloc*  *para dwAlloc*  e  *ltidAlloc,*  respectivamente, e define  *dwNextAlloc*  e  *ltidNextAlloc*  como NULL. 
  
Um provedor que envolve o provedor de armazenamento PST deve verificar  *periodicamente ltidNextAlloc*  para ver se ele é NULL. Se estiver, o provedor deve preencher com um novo GUID e redefinir  *dwNextAlloc*  para que mais IDs de entrada possam ser alocadas. 
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[LTID](ltid.md)

