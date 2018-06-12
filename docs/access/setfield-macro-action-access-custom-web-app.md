---
title: Ação de Macro Definircampo (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 9ae292b0-fde0-4c2b-ba23-23e90365597d
description: A ação Definircampo pode ser usada para atribuir um valor a um campo.
ms.openlocfilehash: 1221ea408540a960b948d2d3ece272fd71cb3daf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765230"
---
# <a name="setfield-macro-action-access-custom-web-app"></a>Ação de Macro Definircampo (aplicativo da web personalizado do Access)

A ação **DefinirCampo** pode ser usada para atribuir um valor a um campo. 
  
> [!IMPORTANT]
> [!IMPORTANTE] A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
> [!NOTE]
> [!OBSERVAçãO] A ação **DefinirCampo** está disponível somente em Macros de Dados. 
  
## <a name="setting"></a>Configuração

A ação **DefinirCampo** tem os seguintes listados na tabela a seguir. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
|**Name** <br/> |Uma cadeia de caracteres que identifica o campo.  <br/> |
|**Valor** <br/> |Uma expressão que especifica o valor a ser atribuído ao campo.  <br/> |
   
## <a name="remarks"></a>Coment�rios

A ação **Definircampo** não pode ser usada fora de um bloco de dados **[CriarRegistro](createrecord-data-block-access-custom-web-app.md)** ou **[EditarRegistro](editrecord-data-block-access-custom-web-app.md)** . 
  

