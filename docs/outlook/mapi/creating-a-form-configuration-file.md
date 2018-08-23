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
ms.openlocfilehash: d8159d93aef020d7c9c1b56be4cf6256f80b8aa3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584161"
---
# <a name="creating-a-form-configuration-file"></a>Criar um arquivo de configuração de formulário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um arquivo de configuração de formulário fornece informações sobre um formulário para o gerente de formulário que está sendo usada e aplicativos cliente. Um arquivo de configuração do formulário contém uma especificação extensiva para um formulário, incluindo as propriedades publicadas pelo formulário para uso por clientes, os verbos implementados pelo formulário e as plataformas compatíveis com o formulário de mensagens.
  
Um arquivo de configuração do formulário é um arquivo com uma extensão. cfg e tem um formato semelhante a um arquivo de inicialização do Windows. É um arquivo de texto sem formatação com um número de seções. Cada seção começa com um nome de seção, colocado entre colchetes. Cada seção contém uma ou mais linhas que definem os valores e configurações relevantes dessa seção. Valores tem um dos seguintes tipos:
  
- Cadeia de caracteres
    
- Cadeia de caracteres exibida
    
- Cadeia de caracteres de plataforma
    
- Nome do caminho
    
- Inteiro
    
- GUID
    
Para obter mais informações sobre as seções de um arquivo. cfg, consulte o [Arquivo de formato do formulário arquivos de configuração](file-format-of-form-configuration-files.md).
  
## <a name="see-also"></a>Confira também



[Desenvolver servidores de formulário MAPI](developing-mapi-form-servers.md)

