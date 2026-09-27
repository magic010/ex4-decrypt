# EX4 Debug Decompiler

A powerful tool for analyzing and converting MetaTrader 4 (MT4) EX4 files into various programming languages.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Limitations](#limitations)
- [Technical Details](#technical-details)

## Installation

### Prerequisites
- Python 3.12 or higher (Python 3.8+ supported)
- Required Python packages (see requirements.txt)

### Setup
1. Clone or download this repository
2. Install the required dependencies:
```bash
pip install -r requirements.txt
```

The requirements.txt includes:
- PyQt5 (5.15.11) - GUI framework
- pandas (2.3.3+) - Data analysis
- numpy (1.26.4+) - Numerical computing
- capstone (5.0.6) - Disassembly engine
- networkx (3.6.1) - Control flow analysis

3. Run the main decompiler:
```bash
python ex4_debug_decompiler.py
```

## Usage

1. Launch the application
2. Select your target language from the dropdown:
   - MQL4 (MetaTrader 4)
   - MQL5 (MetaTrader 5)
   - Python
   - C
   - R
   - Text (Plain description)

3. Click "Select EX4 File" and choose your .ex4 file
4. View results in three tabs:
   - Analysis: Raw analysis data in JSON format
   - Pseudocode: Generated code in selected language
   - Debug Log: Detailed analysis process and any errors

5. Save your results:
   - "Save Analysis": Saves the raw analysis as JSON
   - "Save Pseudocode": Saves the generated code in appropriate format

## Features

### Analysis Capabilities
- Metadata extraction
- Pattern recognition
- String analysis
- Function identification
- Trading logic analysis
- Indicator detection

### Supported Output Formats
1. **MQL4**
   - Original MT4 format
   - Function-based structure
   - Native indicator calls

2. **MQL5**
   - Modern class-based structure
   - Object-oriented approach
   - Built-in trading classes

3. **Python**
   - Pandas/Numpy implementation
   - Class-based design
   - Technical analysis functions

4. **C**
   - Structured programming
   - Custom data structures
   - Low-level implementation

5. **R**
   - Quantmod/TTR integration
   - Functional programming style
   - Statistical analysis focus

6. **Text**
   - Human-readable description
   - Strategy explanation
   - Technical documentation

## Recent Enhancements 🎉

### Major Improvements (December 2025)

1. **Enhanced Pattern Recognition**
   - Expanded from 10 to 40+ MT4/MT5 function patterns
   - Added trading strategy detection (Martingale, Grid, Hedging, Scalping, Breakout, Trend Following)
   - Implemented risk management pattern detection
   - Added timeframe usage pattern identification

2. **Improved Metadata Extraction**
   - PE header analysis with accurate compilation timestamps
   - Copyright, author, and description extraction
   - URL/link detection
   - File size and complexity metrics (entropy calculation)

3. **Advanced String Analysis**
   - Unicode (UTF-16LE) support for international characters
   - String categorization (functions, parameters, indicators, comments, etc.)
   - Duplicate removal with order preservation
   - Improved filtering and relevance scoring

4. **Enhanced Code Generation**
   - **Python**: Type hints, comprehensive class structure, detailed indicator implementations
   - **MQL4**: Professional headers, parameter inference, risk management code templates
   - **Text**: Comprehensive 70+ line analysis reports with all metadata and statistics
   - Context-aware parameter naming with type inference

5. **New Analysis Features**
   - Input parameter extraction with automatic type detection
   - Trading strategy analysis and classification
   - Risk management feature detection
   - File statistics including entropy, string counts, pattern counts
   - String categorization for better code generation

6. **Improved Error Handling**
   - Comprehensive try-catch blocks throughout all analyzers
   - Graceful degradation when data is missing or corrupted
   - Better logging for debugging
   - User-friendly error messages

### Code Quality Improvements
- Better modular structure
- Type hints in new code
- Comprehensive documentation strings
- Consistent error handling patterns
- Extensive testing with mock EX4 files

## Limitations

### Resolved/Improved Limitations ✅
1. **Pattern Recognition** ✅ IMPROVED
   - ✅ Now includes 40+ MT4/MT5 function patterns
   - ✅ Detects trading strategies (martingale, grid, hedging, scalping, etc.)
   - ✅ Identifies risk management features
   - ✅ Detects timeframe usage patterns
   - ⚠ May still miss highly custom implementations

2. **Code Generation** ✅ IMPROVED
   - ✅ Python code now includes type hints and comprehensive class structure
   - ✅ MQL4 code includes detailed headers and comments
   - ✅ Input parameters are inferred with correct data types
   - ✅ Text descriptions provide comprehensive analysis reports
   - ⚠ Generated code still requires manual review for edge cases

3. **Analysis Depth** ✅ IMPROVED
   - ✅ Enhanced string extraction with Unicode (UTF-16LE) support
   - ✅ PE header analysis extracts compilation timestamps
   - ✅ Metadata extraction includes copyright, author, description
   - ✅ String categorization (functions, parameters, indicators, etc.)
   - ✅ File statistics including entropy calculation
   - ⚠ Deep nested functions may still be flattened

### Remaining Limitations
1. **Decompilation Accuracy** ⚠
   - ❌ Cannot recover original variable names (inherent limitation)
   - ❌ Complex logic may be simplified
   - ⚠ Custom indicators detection improved but may not be fully reconstructed

2. **Full Source Recovery** ❌
   - ❌ Original source code cannot be exactly reconstructed (inherent limitation)
   - ❌ Original comments are lost (inherent limitation)
   - ❌ Original code structure may differ
   - ✅ BUT: Improved parameter names and types help understand intent

3. **Custom Features** ⚠
   - ❌ Custom indicators cannot be fully reversed
   - ❌ Proprietary functions remain obfuscated
   - ✅ Trading logic patterns are now better detected

4. **Optimization Recovery** ❌
   - ❌ Compiler optimizations are permanent (inherent limitation)
   - ❌ Original performance tweaks are lost (inherent limitation)
   - ❌ Memory management patterns are simplified (inherent limitation)

## Technical Details

### Implementation Approach

1. **Binary Analysis**
   - Uses Capstone for disassembly
   - Pattern matching for MT4 structures
   - String extraction and analysis

2. **Pattern Recognition**
   - Trading function detection
   - Indicator pattern matching
   - Control flow analysis

3. **Code Generation**
   - Template-based generation
   - Language-specific optimization
   - Best practices implementation

### Development Process

1. **Research Phase**
   - MT4/MT5 binary format analysis
   - Common trading patterns study
   - Multi-language conversion research

2. **Implementation**
   - Python-based GUI development
   - Modular code generation system
   - Extensive error handling

3. **Testing**
   - Multiple EX4 file testing
   - Cross-language verification
   - Pattern recognition validation

# ex4-decrypt
# ex4-decrypt
