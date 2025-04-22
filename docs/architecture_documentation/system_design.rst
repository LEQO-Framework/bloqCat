System Architecture
===================

bloqCat is built as a modular, extendable pipeline. The main components are:

1. **Parser**  
   - Parses QASM3 files into internal circuit representations

2. **Combiner**  
   - Merges multiple circuits intelligently

3. **Formatter**  
   - Outputs combined circuits in QASM3 format or other supported targets

4. **CLI Interface**  
   - Enables command-line access to all core functionalities

.. image:: ../graphics/architecture_diagram.png
   :alt: bloqCat Architecture
   :width: 600px
