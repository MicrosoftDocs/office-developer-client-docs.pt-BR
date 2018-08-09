---
title: Carregar o estado das pastas
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270b1df0-c5cd-0d0f-7b57-2726dee978ab
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 82b00a33c5de11b3fc9ccd3bde4cf31c79b99c2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770666"
---
# <a name="upload-folder-state"></a>Carregar o estado das pastas

  
  
**Aplica-se a**: Outlook 
  
 Este tópico descreve o que acontece durante o estado da pasta de carregamento da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de controle de sessão:  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |
|Estrutura de dados relacionados:  <br/> |**[UPFLD](upfld.md)** <br/> |
|Desse estado:  <br/> |[Carregar o estado de hierarquia](upload-hierarchy-state.md) <br/> |
|Com esse estado:  <br/> |Carregar o estado de hierarquia  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinantes. Um cliente partindo de um estado para outro eventualmente deve retornar para o anterior do último. 
  
## <a name="description"></a>Descrição

Nesse estado inicia o carregamento de uma pasta em uma hierarquia que foi especificada em um estado de hierarquia de carregamento anterior. Durante esse estado, o Outlook fornece o objeto folder (se não tiver sido excluída) e os sinalizadores que indica o estado da pasta (novas e movidas, modificados ou excluídos) como parte da estrutura de dados **UPFLD** correspondente. O cliente então carrega essas informações ao servidor. 
  
Se o carregamento for bem-sucedida, o cliente define *ulFlags* **UPFLD** para **UPF_OK**. Outlook depois limpá suas informações internas sobre a solicitação para carregar a pasta. 
  
Quando o carregamento da pasta for encerrada, armazenamento local retorna ao estado de hierarquia de carregamento. Com base na estrutura **[UPHIER](uphier.md)** correspondente para o estado anterior de hierarquia de carregamento, o Outlook determina se para prosseguir com a carregar a pasta próxima e preparar para o próximo estado de pasta de carregamento. 
  
> [!NOTE]
> Se o cliente precisar carregar apenas uma pasta, o cliente pode iniciar a replicação por meio do [estado de sincronizar](synchronize-state.md) sem digitar o estado de hierarquia de carregamento. O cliente define determinados membros de **[sincronização](sync.md)** — *ulFlags* **UPS_UPLOAD_ONLY** e **UPS_ONE_FOLDER** e *feid* a identificação da pasta — informar ao Outlook que apenas uma pasta será carregado. 
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[ESTADO DE SINCRONIZAÇÃO](syncstate.md)

