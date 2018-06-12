---
title: Bloco de dados ParaCadaRegistro (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8ffa0de2-5abb-4375-9fb5-042ce3c21506
description: Um bloco de dados ParaCadaRegistro repete um conjunto de instruções para cada registro em um domínio.
ms.openlocfilehash: 8ad14a01be05de9fb34299e49a9737f2009ef5ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765082"
---
# <a name="foreachrecord-data-block-access-custom-web-app"></a>Bloco de dados ParaCadaRegistro (aplicativo da web personalizado do Access)

Um bloco de dados **ParaCadaRegistro** repete um conjunto de instruções para cada registro em um domínio. 
  
> [!IMPORTANT]
> [!IMPORTANTE] A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
> [!NOTE]
> [!OBSERVAçãO] O bloco de dados **ParaCadaRegistro** está disponível somente em Macros de Dados. 
  
## <a name="setting"></a>Configuração

A ação **ParaCadaRegistro** tem os seguintes argumentos. 
  
|**Nome do argumento**|**Obrigatório**|**Descrição**|
|:-----|:-----|:-----|
|**Em** <br/> |Sim  <br/> |Uma cadeia de caracteres que identifica o domínio de registros para operar em. O argumento *em* pode conter o nome da tabela, uma consulta seleção ou uma instrução SQL.  <br/> **Observação**: O domínio especificado não pode incluir dados armazenados em uma tabela vinculada ou fonte de dados ODBC.           |
|**Condição onde** <br/> |Não  <br/> |Uma expressão de cadeia de caracteres usada para restringir o intervalo de dados no qual o bloco de dados **ParaCadaRegistro** é executada. Por exemplo, critérios costuma ser equivalente à cláusula WHERE em uma expressão SQL, sem a palavra onde. Se os critérios forem omitidos, o bloco de dados **ParaCadaRegistro** opera em todo o domínio especificado pelo argumento *em* . Qualquer campo que está incluído nos critérios também deve ser um campo no *In* .  <br/> |
|**Alias** <br/> |Não  <br/> |Uma cadeia de caracteres que fornece um nome alternativo para o domínio especificado pelo argumento *em* . Frequentemente usado para reduzir o nome da tabela referências posteriores evitar possíveis referências ambíguas. Se o *Alias* não for especificado, o nome da tabela ou consulta será usado como o alias.  <br/> |
   
## <a name="remarks"></a>Comentários

Use a ação **[SairparaCadaRegistro](exitforeachrecord-macro-action-access-custom-web-app.md)** para encerrar um bloco de dados **ParaCadaRegistro** imediatamente. 
  

