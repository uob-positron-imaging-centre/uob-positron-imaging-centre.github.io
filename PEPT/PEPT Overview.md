---
layout: page
title: PEPT Overview
permalink: /PEPT Overview/
parent: PEPT
has_children: false
---

# Positron Emission Particle Tracking (PEPT)
{: .fs-9 }

[Original Source Text](https://www.birmingham.ac.uk/research/activity/physics/particle-nuclear/positron-imaging-centre/positron-emission-particle-tracking-pept/pept-overview.aspx).
{: .fs-6 .fw-300 }

The Positron Emission Particle Tracking (PEPT) technique was invented here at the University of Birmingham and is a variant of the medical imaging technique positron emission tomography (PET) which is used in nuclear medicine. The difference for PEPT is that a single radioactively labelled tracer particle is used and rather than generating an image, the aim is to determine the location of the individual particle accurately and frequently as it moves within a piece of equipment.

The Forte camera system has the capability to locate a tracer travelling at 1m/s to within 0.5mm approximately 250 times a second. The maximum speed at which the particle can be tracked accurately depends on a variety of factors such as how active the particle is and the amount and density of ‘extra material’ between the particle and the detectors so this is considered on a case by case basis.

Tracking can be carried out inside equipment provided it can be set up between the detectors. The field of view being 80x50x40cm³ for the Forte camera (please see the ADAC Forte Positron Camera for full dimensions).  For more awkward pieces of equipment the Modular Positron Camera is an option which can be arranged in multiple different geometries. The gamma-rays emitted by the tracer are quite penetrating, 50% will pass through 11mm steel, so tracking is possible inside real process equipment.

A radioisotope is incorporated into a tracer particle (most typically Fluorine-18) which undergoes beta decay involving emission of a positron. Once emitted from the nucleus, the positron annihilates with an electron, releasing energy in the form of two 511keV gamma photons which are emitted back-to-back, 180° apart to within 0.5°.
![PEPT](https://www.birmingham.ac.uk/Images/College-EPS-only/nuclear/positron-imaging-centre/positron-emitting-radioscope-diagram.png)
The tracer particle is introduced into the system of study which is mounted between the detectors of the positron camera. Each detector is able to detect incident gamma-rays and determine their interaction coordinates to within a few mm. Only ‘coincidence events’ where gamma-rays are detected simultaneously are recorded; from a small number of these events the tracer position can be determined through triangulation. In practice, typically 50-100 events are used to determine each location to ensure accuracy.

The necessary radioisotopes for PEPT to fabricate the tracer particles are produced using the MC40 Cyclotron located next to the Centre at the University of Birmingham. A variety of shapes and sizes of tracer particles can be used, generally speaking the range being between 100µm-10mm. (Please see Radioactively Labelled Tracers for more information or contact the Centre directly.)

The data produced from PEPT is processed using an algorithm developed at Birmingham that removes ‘corrupt events’ that occur due to detection of random coincidences or scattered photons. 

After processing, the result is a sequence of locations in the form (t, x, y, z) representing the path of the tracer. These locations can then be used to extract useful information such as time averaged velocity fields, instantaneous velocity, residence times, dispersion coefficients and more.
