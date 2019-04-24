---
title: Carregar estado da pasta
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270b1df0-c5cd-0d0f-7b57-2726dee978ab
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c20f2998a2fef1ddb53b13708dcf56f9d7b50dbe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348423"
---
# <a name="upload-folder-state"></a>Carregar estado da pasta

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Este tópico descreve o que acontece durante o estado da pasta de carregamento da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de Estado:  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |
|Estrutura de dados relacionada:  <br/> |**[UPFLD](upfld.md)** <br/> |
|A partir deste Estado:  <br/> |[Estado de hierarquia de upload](upload-hierarchy-state.md) <br/> |
|Para este Estado:  <br/> |Estado de hierarquia de upload  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinista. Um cliente que faz parte de um estado para outro deve eventualmente retornar para o primeiro a partir do último. 
  
## <a name="description"></a>Descrição

Este estado inicia o carregamento de uma pasta em uma hierarquia que tenha sido especificada em um estado de hierarquia de carregamento anterior. Durante esse Estado, o Outlook fornece o objeto Folder (se ele não tiver sido excluído) e os sinalizadores que indicam o estado da pasta (novo, movido, modificado ou excluído) como parte da estrutura de dados **UPFLD** correspondente. O cliente carrega essas informações no servidor. 
  
Se o upload for bem-sucedido, o cliente define *parâmetroulflags* no **UPFLD** como **UPF_OK**. O Outlook, em seguida, limpa suas informações internas sobre a solicitação para carregar a pasta. 
  
Quando o carregamento da pasta termina, o repositório local retorna ao estado de hierarquia de upload. Com base na estrutura **[UPHIER](uphier.md)** correspondente ao estado de hierarquia de carregamento anterior, o Outlook determina se deve continuar carregando a próxima pasta e se preparar para o próximo estado de pasta de carregamento. 
  
> [!NOTE]
> Se o cliente precisar carregar apenas uma pasta, o cliente poderá iniciar a replicação por meio do [estado de sincronização](synchronize-state.md) sem entrar no estado de hierarquia de carregamento. O cliente define determinados membros de **[Sync](sync.md)** — *parâmetroulflags* para **UPS_UPLOAD_ONLY** e **UPS_ONE_FOLDER** e *feid* para a ID da pasta, para informar ao Outlook que apenas uma pasta será carregada. 
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

