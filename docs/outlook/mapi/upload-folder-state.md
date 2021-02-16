---
title: Estado carregar pasta
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270b1df0-c5cd-0d0f-7b57-2726dee978ab
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c20f2998a2fef1ddb53b13708dcf56f9d7b50dbe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419566"
---
# <a name="upload-folder-state"></a>Estado carregar pasta

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Este tópico descreve o que acontece durante o estado da pasta de carregamento da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de Estado:  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |
|Estrutura de dados relacionada:  <br/> |**[UPFLD](upfld.md)** <br/> |
|Desse estado:  <br/> |[Estado de hierarquia de carregamento](upload-hierarchy-state.md) <br/> |
|Para esse estado:  <br/> |Estado de hierarquia de carregamento  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinística. Um cliente que sai de um estado para outro eventualmente deve retornar ao primeiro do último. 
  
## <a name="description"></a>Descrição

Esse estado inicia o carregamento de uma pasta em uma hierarquia que foi especificada em um estado de hierarquia de carregamento anterior. Durante esse estado, o Outlook fornece o objeto folder (se não tiver sido excluído) e os sinalizadores que indicam o estado da pasta (nova, movida, modificada ou excluída) como parte da estrutura de dados **UPFLD** correspondente. Em seguida, o cliente carrega essas informações no servidor. 
  
Se o upload for bem-sucedido, o cliente  *define ulFlags* **em UPFLD** como **UPF_OK**. Em seguida, o Outlook limpa suas informações internas sobre a solicitação para carregar a pasta. 
  
Quando o carregamento da pasta termina, o armazenamento local retorna ao estado de hierarquia de carregamento. Com base na estrutura **[UPHIER](uphier.md)** correspondente ao estado de hierarquia de upload anterior, o Outlook determina se deve prosseguir com o carregamento da próxima pasta e se preparar para o próximo estado de pasta de carregamento. 
  
> [!NOTE]
> Se o cliente precisar carregar apenas uma pasta, o cliente poderá iniciar a replicação por meio do estado de sincronização [sem](synchronize-state.md) inserir o estado de hierarquia de carregamento. O cliente define determinados membros de **[SYNC](sync.md)** — *ulFlags*  como **UPS_UPLOAD_ONLY** e **UPS_ONE_FOLDER** e se ajusta à ID da pasta — para dizer ao Outlook que apenas uma pasta será carregada. 
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

