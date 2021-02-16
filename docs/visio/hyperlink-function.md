---
title: Função HYPERLINK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251441
localization_priority: Normal
ms.assetid: 943636a6-e135-a626-7924-11e238156548
description: Navega até o endereço especificado, que pode ser um arquivo, UNC ou caminho da URL.
ms.openlocfilehash: 5e4952c3d56eff0cb1e6518928a7b8259f645046
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329943"
---
# <a name="hyperlink-function"></a>Função HYPERLINK

Navega até o endereço especificado, que pode ser um arquivo, UNC ou caminho da URL.
  
## <a name="syntax"></a>Sintaxe

HYPERLINK(" ** *endereço* ** "[," ** *subddress* ** "," ** *extrainfo* ** ", ** *window* **," ** *frame* ** "]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _address_ <br/> |Obrigatório  <br/> |**String** <br/> |Um caminho completo ou relativo.  <br/> |
| _subaddress_ <br/> |Opcional  <br/> |**String** <br/> |Especifica uma localização no address ao qual se vincular. Por exemplo, se o address for um arquivo do Microsoft Visio, o subaddress poderá ser um nome de página; se for um arquivo do Microsoft Excel, o subaddress poderá ser uma planilha ou um intervalo na planilha; se for uma URL de uma página HTML, o subaddress poderá ser uma âncora.  <br/> |
| _extrainfo_ <br/> |Opcional  <br/> |**String** <br/> |Passa as informações utilizadas para resolver o URL, como as coordenadas de um mapa de imagens.  <br/> |
| _janela_ <br/> |Opcional  <br/> |**Boolean** <br/> |Especifica se o hiperlink será aberto em uma nova janela. O valor padrão é FALSO.  <br/> |
| _frame_ <br/> |Opcional  <br/> |**String** <br/> | Especifica o nome de uma moldura para servir de destino quando o Visio for aberto como um documento ativo em um navegador ActiveX, como o Microsoft Internet Explorer 3.0 ou superior. O padrão é uma cadeia de caracteres vazia.  <br/> |
   
## <a name="remarks"></a>Comentários

Se o documento não tiver caminho de base, o Visio navegará de acordo com o caminho do documento. Se o documento não tiver sido salvo, o hiperlink não será definido. 
  
Caminhos relativos têm como base o campo **Base do Hiperlink** especificado na caixa de diálogo **Propriedades do Visio**. 
  
Utilize a função GOTOPAGE para navegar em páginas de um documento. 
  
## <a name="example-1"></a>Exemplo 1

 `HYPERLINK("C:\My Documents\Drawing1.vsdx")`
  
## <a name="example-2"></a>Exemplo 2

 `HYPERLINK("\\Server\Share\Drawing1.vsdx")`
  
## <a name="example-3"></a>Exemplo 3

 `HYPERLINK("https://www.microsoft.com")`
  
## <a name="example-4"></a>Exemplo 4

 `HYPERLINK("..\data.xlsx","sheet1!A1")`
  

