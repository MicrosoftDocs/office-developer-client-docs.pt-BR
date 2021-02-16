---
title: Bloco de dados ForEachRecord (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8ffa0de2-5abb-4375-9fb5-042ce3c21506
description: Um bloco de dados ForEachRecord repete um conjunto de instruções para cada registro em um domínio.
ms.openlocfilehash: 9715824bff7d478fa2880ada5e8770f7a0c88883
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428232"
---
# <a name="foreachrecord-data-block-access-custom-web-app"></a>Bloco de dados ForEachRecord (aplicativo Web personalizado do Access)

Um **bloco de dados ForEachRecord** repete um conjunto de instruções para cada registro em um domínio. 
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
> [!NOTE]
> O bloco de dados **ParaCadaRegistro** está disponível somente em Macros de Dados. 
  
## <a name="setting"></a>Setting

A ação **ParaCadaRegistro** tem os seguintes argumentos. 
  
|**Nome do argumento**|**Obrigatório**|**Descrição**|
|:-----|:-----|:-----|
|**Em** <br/> |Sim  <br/> |Uma cadeia de caracteres que identifica o domínio de registros a ser utilizado. O  *argumento In*  pode conter o nome da tabela, uma consulta seleção ou uma instrução SQL.  <br/> **OBSERVAÇÃO:** o domínio especificado não pode incluir dados armazenados em uma tabela vinculada ou fonte de dados ODBC.           |
|**Condição Where** <br/> |Não  <br/> |Uma expressão de cadeia de caracteres usada para restringir o intervalo de dados no qual o bloco de dados **ForEachRecord** é executado. Por exemplo, os critérios geralmente são equivalentes à cláusula WHERE em uma expressão SQL, sem a palavra WHERE. Se os critérios são omitidos, o bloco de dados **ForEachRecord** opera em todo o domínio especificado pelo  *argumento*  In. Qualquer campo incluído nos critérios também deve ser um campo em  *In*  .  <br/> |
|**Alias** <br/> |Não  <br/> |Uma cadeia de caracteres que fornece um nome alternativo para o domínio especificado pelo  *argumento*  In. Comumente usado para reduzir o nome da tabela para subsequentes referências, evitando referências ambíguas. Se  *Alias*  não for especificado, o nome da tabela ou consulta será usado como o alias.  <br/> |
   
## <a name="remarks"></a>Comentários

Use a ação **[SairparaCadaRegistro](exitforeachrecord-macro-action-access-custom-web-app.md)** para encerrar um bloco de dados **ParaCadaRegistro** imediatamente. 
  

