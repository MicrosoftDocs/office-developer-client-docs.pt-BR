---
title: Adicionar e fazer referência a assemblies personalizados
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- modelos de formulário compatíveis com o InfoPath 2003, usando assemblies personalizados, assemblies [InfoPath 2007], adicionando personalizado usando o modelo de objeto do InfoPath 2003
localization_priority: Normal
ms.assetid: 20e1f43e-8279-48fc-8f34-16a2729dbc9b
description: Quando você adiciona uma referência a um assembly personalizado em um projeto de modelo de formulário de código gerenciado, esse assembly é incluído no arquivo de modelo de formulário (. xsn) quando seu projeto é compilado e publicado.
ms.openlocfilehash: 19b5f06231bb03cfac8b32b157e03956b5fc334e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431166"
---
# <a name="add-and-reference-custom-assemblies"></a>Adicionar e fazer referência a assemblies personalizados

Quando você adiciona uma referência a um assembly personalizado em um projeto de modelo de formulário de código gerenciado, esse assembly é incluído no arquivo de modelo de formulário (. xsn) quando seu projeto é compilado e publicado.
  
## <a name="add-and-reference-a-custom-assembly"></a>Adicionar e referenciar um assembly personalizado

Para evitar um conflito com o modo como o sistema de projeto do InfoPath gerencia arquivos que são adicionados ao arquivo de modelo de formulário, não copie qualquer assembly personalizado que você deseja fazer referência à pasta de nível superior de um projeto de modelo de formulário. Por padrão, este será um caminho no seguinte formato: < *drive* >: \Users\ *username* \Documents\InfoPath Projects \ *ProjectName* 
  
Se você deseja mover assemblies personalizados que você faz referência a um local dentro da pasta do projeto, você deve criar uma subpasta na pasta principal do projeto e, em seguida, copiar e fazer referência a assemblies personalizados dessa subpasta. No enTanto, lembre-se de que a criação de uma subpasta para assemblies referenciados não é necessária. Desde que um assembly referenciado não esteja localizado dentro da pasta de nível superior do projeto, o sistema de projeto do InfoPath copiará o assembly para o arquivo de modelo de formulário (. xsn) quando o projeto for compilado e publicado.
  
### <a name="reference-a-custom-assembly-from-its-default-location"></a>Fazer referência a um assembly personalizado do local padrão

1. Abra o projeto de modelo de formulário no Visual Studio 2012.
    
2. On the **Project** menu, click **Add Reference**.
    
3. Clique na guia **procurar** , localize e especifique o assembly e, em seguida, clique em **OK** para adicionar a referência. 
    
## <a name="see-also"></a>Confira também

#### <a name="tasks"></a>Tarefas

[Criar um modelo de formulário usando o modelo de objeto do InfoPath 2003](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)

