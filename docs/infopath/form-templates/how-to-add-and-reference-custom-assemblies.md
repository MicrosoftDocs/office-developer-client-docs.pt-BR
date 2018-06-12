---
title: Adicione e referência Assemblies personalizados
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- modelo de objeto de modelos de formulário de 2003 compatíveis do InfoPath, usando assemblies personalizados, assemblies [InfoPath 2007], adição personalizada usando o InfoPath 2003
localization_priority: Normal
ms.assetid: 20e1f43e-8279-48fc-8f34-16a2729dbc9b
description: Quando você adiciona uma referência a um assembly personalizado em um projeto de modelo de formulário de código gerenciado, nesse assembly é incluído dentro do arquivo de modelo de formulário (. xsn) quando o projeto é compilado e publicado.
ms.openlocfilehash: e182930ebe14b6f64d1b90509fe400cc1fb1b26e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765599"
---
# <a name="add-and-reference-custom-assemblies"></a>Adicione e referência Assemblies personalizados

Quando você adiciona uma referência a um assembly personalizado em um projeto de modelo de formulário de código gerenciado, nesse assembly é incluído dentro do arquivo de modelo de formulário (. xsn) quando o projeto é compilado e publicado.
  
## <a name="add-and-reference-a-custom-assembly"></a>Adicionar e fazer referência a um Assembly personalizado

Para evitar um conflito com como o sistema de projeto do InfoPath gerencia arquivos que são adicionados ao arquivo de modelo de formulário, não copie qualquer assemblies personalizados que você deseja fazer referência para a pasta de nível superior de um projeto de modelo de formulário. Por padrão, este será um caminho no seguinte formato: < *unidade* >: \Users\ \Documents\InfoPath Projects\ *UserName* *NomeDoProjeto* 
  
Se desejar mover assemblies personalizados que você faz referência a um local dentro da pasta do projeto, você deve criar uma subpasta na pasta do projeto principal e copie e assemblies personalizados de referência da subpasta. No entanto, lembre-se de que a criação de uma subpasta para assemblies referenciados não é necessário. Desde que um assembly referenciado não está localizado na pasta de nível superior do projeto, o sistema de projeto do InfoPath copiará o assembly para o arquivo de modelo de formulário (. xsn) quando o projeto é compilado e publicado.
  
### <a name="reference-a-custom-assembly-from-its-default-location"></a>Referência a um assembly personalizado do local padrão

1. Abra o projeto de modelo de formulário no Visual Studio 2012.
    
2. On the **Project** menu, click **Add Reference**.
    
3. Clique na guia **Procurar** , localize especificar o assembly e clique em **Okey** para adicionar a referência. 
    
## <a name="see-also"></a>Ver também

#### <a name="tasks"></a>Tarefas

[Criar um modelo de formulário usando o modelo de objeto do InfoPath 2003](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)

