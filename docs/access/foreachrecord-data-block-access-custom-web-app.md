---
title: Bloco de dados ParaCadaRegistro (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8ffa0de2-5abb-4375-9fb5-042ce3c21506
description: Um bloco de dados ParaCadaRegistro repete um conjunto de instruções para cada registro em um domínio.
ms.openlocfilehash: 9715824bff7d478fa2880ada5e8770f7a0c88883
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302454"
---
# <a name="foreachrecord-data-block-access-custom-web-app"></a>Bloco de dados ParaCadaRegistro (aplicativo Web personalizado do Access)

Um bloco de dados **ParaCadaRegistro** repete um conjunto de instruções para cada registro em um domínio. 
  
> [!IMPORTANT]
> [!IMPORTANTE] A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
> [!NOTE]
> O bloco de dados **ParaCadaRegistro** está disponível somente em Macros de Dados. 
  
## <a name="setting"></a>Configuração

A ação **ParaCadaRegistro** tem os seguintes argumentos. 
  
|**Nome do argumento**|**Obrigatório**|**Descrição**|
|:-----|:-----|:-----|
|**No** <br/> |Sim  <br/> |Uma cadeia de caracteres que identifica o domínio de registros a ser utilizado. O argumento *in* pode conter o nome da tabela, uma consulta seleção ou uma instrução SQL.  <br/> **Observação**: o domínio especificado não pode incluir dados armazenados em uma tabela vinculada ou fonte de dados ODBC.           |
|**Condição Where** <br/> |Não  <br/> |Uma expressão de cadeia de caracteres usada para restringir o intervalo de dados no qual o bloco de dados **ParaCadaRegistro** é executado. Por exemplo, os critérios geralmente são equivalentes à cláusula WHERE em uma expressão SQL, sem a palavra WHERE. Se os critérios forem omitidos, o bloco de dados **ParaCadaRegistro** funcionará em todo o domínio especificado pelo argumento *in* . Qualquer campo incluído nos critérios também deve ser um campo no *no* .  <br/> |
|**Alias** <br/> |Não  <br/> |Uma cadeia de caracteres que fornece um nome alternativo para o domínio especificado pelo argumento *in* . Comumente usado para reduzir o nome da tabela para subsequentes referências, evitando referências ambíguas. Se *alias* não for especificado, o nome da tabela ou da consulta será usado como o alias.  <br/> |
   
## <a name="remarks"></a>Comentários

Use a ação **[SairparaCadaRegistro](exitforeachrecord-macro-action-access-custom-web-app.md)** para encerrar um bloco de dados **ParaCadaRegistro** imediatamente. 
  

