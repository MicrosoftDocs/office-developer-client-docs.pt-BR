---
title: Criar um arquivo de configuração de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aaf3b33d-ad2d-4ef8-847f-1ab1eaf08706
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 9ceb7ad347e73f69eca3463ed2edc4438a45a21f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766352"
---
# <a name="creating-a-form-configuration-file"></a>Criar um arquivo de configuração de formulário

  
  
**Aplica-se a**: Outlook 
  
Um arquivo de configuração de formulário fornece informações sobre um formulário para o gerente de formulário que está sendo usada e aplicativos cliente. Um arquivo de configuração do formulário contém uma especificação extensiva para um formulário, incluindo as propriedades publicadas pelo formulário para uso por clientes, os verbos implementados pelo formulário e as plataformas compatíveis com o formulário de mensagens.
  
Um arquivo de configuração do formulário é um arquivo com uma extensão. cfg e tem um formato semelhante a um arquivo de inicialização do Windows. É um arquivo de texto sem formatação com um número de seções. Cada seção começa com um nome de seção, colocado entre colchetes. Cada seção contém uma ou mais linhas que definem os valores e configurações relevantes dessa seção. Valores tem um dos seguintes tipos:
  
- String
    
- Cadeia de caracteres exibida
    
- Cadeia de caracteres de plataforma
    
- Nome do caminho
    
- Inteiro
    
- GUID
    
Para obter mais informações sobre as seções de um arquivo. cfg, consulte o [Arquivo de formato do formulário arquivos de configuração](file-format-of-form-configuration-files.md).
  
## <a name="see-also"></a>Confira também



[Desenvolver servidores de formulário MAPI](developing-mapi-form-servers.md)

