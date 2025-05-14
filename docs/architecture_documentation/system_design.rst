System Architecture
===================

bloqCat is built to be modular. The main components are:

1. **Parser**  
   - Parses QASM3 files into internal circuit representations

2. **Combiner**  
   - Merges multiple circuits intelligently

3. **Formatter**  
   - Outputs combined circuits in QASM3 format.

4. **REST API**  
   - Enables command-line access to all core functionalities

.. image:: ../graphics/architecture_diagram.png
   :alt: bloqCat Architecture
   :width: 600px
